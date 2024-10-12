### **Server Network Recording (SNR) in League of Legends: A Technical Overview**

### [Original Text - Determinism in League of Legends: Implementation](https://technology.riotgames.com/news/determinism-league-legends-implementation)

In large-scale online games like *League of Legends*, maintaining server stability and addressing bugs efficiently are critical to ensuring a smooth player experience. One of the most powerful tools developed to support these goals is the **Server Network Recording (SNR)** system. This system enables precise capture and replay of game states, facilitating accurate debugging, disaster recovery, and overall system optimization.

#### **Overview of Server Network Recording (SNR)**

The primary challenge that the SNR system addresses is **non-deterministic behavior** in a server environment. In a deterministic system, the same inputs consistently produce the same outputs, but in a complex multiplayer environment, various factors such as player inputs, network latency, and random events introduce non-determinism. This variability complicates bug tracking and resolution, as reproducing the exact conditions that led to an issue can be difficult.

The SNR system solves this problem by recording **all uncontrolled inputs**, including player actions (movement, abilities, attacks) and network traffic. This data is stored frame-by-frame during the game session. In the event of a bug or crash, developers can replay the captured inputs, enabling them to recreate the exact state of the game for analysis and debugging.

#### **SNR Architecture: Recording and Playback**

The SNR system consists of two fundamental processes: **Recording** and **Playback**.

1. **Recording**: During live gameplay, the server continuously records incoming network traffic and player inputs. Each frame of the game is captured as part of a sequential timeline, ensuring that all relevant data for reproducing game states is preserved. The captured data includes actions such as player movements, spell casts, attacks, and any other inputs that could influence the game state.

2. **Playback**: When a bug or issue needs to be investigated, the recorded timeline can be played back. This allows developers to reconstruct the exact sequence of events, replicating the game state as it was during live play. This replay process is crucial for identifying the root cause of bugs, as it removes uncertainty by presenting an identical recreation of the original environment.

#### **Technical Benefits of SNR**

The SNR system introduces several key advantages for both development and operational stability:

- **Precision in Debugging**: The ability to isolate the exact frame in which a bug occurs enables fine-grained analysis. Developers can step through the exact sequence of events that led to an issue, significantly improving debugging efficiency.

- **Reproducibility of Non-Deterministic Issues**: One of the primary challenges in multiplayer game development is replicating non-deterministic issues. SNR solves this by providing a reliable way to recreate the same inputs and server responses, making it possible to reproduce even the most elusive bugs.

- **Disaster Recovery**: SNR also plays a role in **Disaster Recovery (DDR)**. In the event of a server failure or crash, the recorded timeline can be used to restore the server state to a point just before the failure, minimizing downtime and data loss.

#### **Challenges in Implementing SNR**

While the concept of SNR is straightforward, its implementation required overcoming several technical challenges:

- **Client State Simulation**: During playback, it is essential to accurately simulate the client state, as the original network traffic will not be present. This was accomplished by introducing **fake client endpoints**. These endpoints mimic real clients' behavior, allowing the server to process the recorded data as though the clients were still connected. This approach ensures that the recorded frames are accurately replayed, without requiring live player connections.

- **Handling Network Traffic**: One of the critical decisions in the SNR system was how to capture network traffic. Rather than recording at the lowest level of the network stack, SNR captures the traffic at an application layer, focusing on higher-level gameplay messages. This avoids unnecessary complexity while still capturing all relevant data for gameplay state replication.

#### **Future Applications of SNR**

The potential of SNR extends beyond its current use cases in debugging and disaster recovery. Future applications could include:

- **Performance Profiling and Optimization**: By replaying recorded game sessions, developers can analyze server performance under specific conditions, identify bottlenecks, and optimize resource usage.

- **Game Balance Testing**: SNR could be employed to test how new patches or changes affect gameplay by replaying previous game sessions with modified mechanics. This would provide a controlled environment for balance testing.