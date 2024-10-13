# Game Design Concepts
#### **Prerequisite**

Understanding **game design** requires knowledge of two core aspects:

1. **Game Mechanics**: The systems, rules, and technical elements that dictate how a game operates. These include player interactions, AI, physics, and progression.
2. **Game Narratives**: The story, lore, characters, and emotional engagement in the game. These elements create the thematic framework and player motivation.

Balancing mechanics and narratives in a meaningful way is key to crafting a cohesive and immersive gaming experience.


#### **Summary**

The document "Game Design Concepts" provides insights into the integration of mechanics and narratives in game design, along with key models and structures for AI, character behavior, and world-building. It discusses ten core ideas to enhance both gameplay and storytelling, ensuring that game mechanics and narratives work in harmony to create immersive and engaging player experiences. Topics include emotional AI modeling, modular behavior trees, and dynamic game world design, with an emphasis on flexibility and strategic depth.


#### **Key Points**

1. **Mechanical Narratives**: Elements in a game that simultaneously fulfill both gameplay and narrative purposes. These allow for cohesive storytelling where players’ actions align with the game's story and mechanics, reducing disconnect between the two.

2. **Sensors, Filters, and Motors**: In AI design, agents are constructed using:
   - **Sensors**: To collect data from the environment.
   - **Filters**: To process and analyze this data.
   - **Motors**: To trigger actions based on the filtered data. This model is scalable for simple or complex AI systems.

3. **Psychological Force Field**: Characters can be influenced by invisible force fields. Repulsive forces push characters away from undesirable entities, while attractive forces draw them toward favorable entities. This system simulates character preferences and behavioral choices.

4. **Parallel-Attention Timeline**: AI multitasking modeled as a two-dimensional grid where each row represents attention priority and each column represents time slots. Characters focus on the most urgent tasks, adding realistic behavior by allowing AI to prioritize actions dynamically.

5. **Partial Movement Constraints**: Restricting enemy movement along predefined pathways (rather than allowing full freedom) makes gameplay more strategic, while also simplifying AI design and reducing computational complexity.

6. **Emotional State Machine**: Characters’ emotional states are modeled in a 3D space with axes representing **happiness**, **excitement**, and **confidence**. As characters’ emotions shift, their behaviors change in real-time, giving depth to character interactions and adding psychological complexity to AI.

7. **Deities of the Game World**: The game world can be governed by different control models resembling theistic worldviews:
   - **Monotheistic**: One centralized control module manages all feedback loops.
   - **Polytheistic**: Multiple modules govern the characters.
   - **Pantheistic**: Characters regulate themselves with no external control, acting as their own feedback systems.

8. **Modular Behavior Tree**: AI behavior can be simplified through modular systems, where individual behaviors are stored in modular trees that attach or detach to characters dynamically during gameplay, allowing adaptable and complex behaviors without overwhelming design structures.

9. **Brand-Building**: A successful game needs a strong brand that consists of:
   - **Purpose**: A clear narrative or goal that motivates the player.
   - **Logic**: Consistency in game systems that make sense within the world.
   - **Mystery**: Opportunities for players to explore and discover, creating intrigue. A well-rounded brand engages players emotionally and ensures long-term success.

10. **Image as a Game Map**: Images can be used to generate game maps. Each pixel in an image can represent a voxel in a game terrain, with attributes like brightness and color determining features such as height, prop density, and biome types. This allows dynamic terrain generation and manipulation during gameplay.


#### **Questions & Answers**

1. **What are Mechanical Narratives, and why are they important?**
   - Mechanical narratives are design elements that simultaneously serve both gameplay mechanics and the story. They prevent ludonarrative dissonance (the disconnect between gameplay and narrative), ensuring players feel immersed and that their actions are meaningful within the game’s world.

2. **How do Sensors, Filters, and Motors enhance AI design?**
   - These components enable AI agents to interact with the environment. Sensors detect data, filters process it, and motors execute the corresponding actions, forming a dynamic system that allows for realistic and responsive AI behavior.

3. **How does the Psychological Force Field work in game design?**
   - Each character in the game can be seen as having an invisible psychological force field. Different entities in the world (such as enemies, allies, or goals) warp this field, causing characters to be repelled by or attracted to them based on preferences, which influences their movement and decision-making.

4. **What is the purpose of the Parallel-Attention Timeline in AI systems?**
   - It allows AI to multitask by prioritizing actions based on attention demand. For example, an AI character might focus more on urgent tasks (like fighting an enemy) while occasionally checking lower-priority tasks (such as monitoring surroundings).

5. **Why are Partial Movement Constraints beneficial in games?**
   - Constraining movement to predefined paths adds strategy and depth to gameplay. It makes levels more interesting while keeping AI design simpler and reducing computational loads.

6. **What is an Emotional State Machine?**
   - A system that tracks characters’ emotional states in a 3D space (happiness, excitement, confidence). Changes in these states dynamically affect how characters behave, giving depth to both AI and storytelling.

7. **How do Deities of the Game World models influence game design?**
   - These models determine how control is exerted over the game world:
     - **Monotheistic**: A single control system manages everything.
     - **Polytheistic**: Multiple controllers manage different elements.
     - **Pantheistic**: Characters self-regulate without external control, giving a more decentralized approach to game design.

8. **What is the advantage of Modular Behavior Trees for AI?**
   - Modular behavior trees break complex behaviors into smaller, reusable modules that can dynamically attach or detach to AI characters during gameplay. This allows for flexible and adaptive behavior, making AI more scalable and manageable.

9. **What is the importance of Brand-Building in game design?**
   - A successful game needs a strong brand identity that resonates with players. By focusing on purpose, logic, and mystery, a game can create a lasting emotional connection with its audience, which is key for long-term engagement and success.

10. **How can images be used to generate game maps?**
   - Images serve as a blueprint for game maps where each pixel represents a unit of terrain (voxel). Features like terrain height, prop density, and biome type can be derived from pixel properties (e.g., brightness, color), allowing for efficient map creation and dynamic manipulation of the environment during gameplay.


#### **Further Reading**

- **"The Art of Game Design: A Book of Lenses" by Jesse Schell** – Offers practical approaches to game design, providing different perspectives on balancing mechanics and narrative.
- **"A Theory of Fun for Game Design" by Raph Koster** – Explores the role of fun in games and how mastering mechanics leads to player satisfaction.
- **"Rules of Play: Game Design Fundamentals" by Katie Salen and Eric Zimmerman** – A comprehensive guide to game design, focusing on the intersection of mechanics, player interaction, and storytelling.
- **"Game Feel: A Game Designer’s Guide to Virtual Sensation" by Steve Swink** – Examines how sensory feedback in games enhances the player’s emotional and tactile connection to the game, contributing to both narrative and mechanical immersion.