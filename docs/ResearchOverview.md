---
title: Research Overview
nav_order: 2
---
Modeling is the process of predicting future states based on current actions, and with a precise model, we can evaluate all possible actions and choose the optimal one. Throughout history, humanity has developed models to describe physical phenomena and used them as the foundation for controlling systems.

The rise of neural network-based modeling-where nonlinear functions are represented by a combination of countless parameters rather than explicit analytical equations-has driven groundbreaking technological advancements. Robotics plays a crucial role in bridging high-performance AI with the physical world. However, unlike in simulation environments, real-world applications face inherent challenges in physical modeling. Our understanding of complex forces such as fluid dynamics and friction remains incomplete, making it difficult to develop robots that can swim like fish, fly like birds, or skate on ice with precision.

Modeling and control raise many fundamental research questions: What is the most effective model we can construct given the available data? How can we integrate prior domain knowledge into neural networks? What kind of data should be collected to improve modeling? How can we assess the uncertainty and robustness of our current models and control policies? These open questions shape our research, where we approach robotics through the lens of modeling and control to find meaningful answers.

Our vision is to develop learning-based policies that are practical and reliable in real-world environments. To achieve this, we focus on advancing modeling techniques, designing control policies with safety and stability guarantees, and improving generalizability so that diverse robots can perform a wide range of tasks.

-------
Modeling
{: .fs-6 }

Modeling is a fundamental challenge across various domains, including sensors, robotics, multi-agent systems, and climate prediction. By designing accurate sensor models or learning to characterize unknown sensor noise, we can achieve high performance even with low-cost sensors, leading to significant cost savings.

Dynamical modeling has been explored through a range of techniques, including generative models based on neural networks, Dynamic Mode Decomposition (DMD), and Gaussian Processes (GP). The effectiveness of these methods depends on factors such as the system’s degree of local linearity and the availability of data. Recently, neural network-based modeling has gained prominence due to the abundance of data, but acquiring high-quality real-world dynamical data remains a major challenge. As a result, researchers are incorporating domain knowledge to enhance model reliability and performance.

For instance, the Koopman model reformulates nonlinear systems into a linear representation, allowing us to leverage well-established linear system theories. This facilitates stability analysis and enables the direct application of control-theoretic principles. In legged robots, for example, the dynamics undergo discrete transitions depending on whether the foot is in contact with the ground or in the air. To model such hybrid systems with neural networks, these mode transitions must be explicitly incorporated.

Many physical systems exhibit intrinsic symmetries, such as translation and rotation, while energy conservation laws-rooted in Noether’s theorem-are tied to continuous symmetries. By leveraging these properties, equivariant neural networks have demonstrated superior modeling performance. Our research focuses on integrating various forms of prior knowledge to improve the modeling of complex, nonlinear, and hybrid robotic systems, ultimately enhancing predictive accuracy and control effectiveness.

--------
Control
{: .fs-6 }

Reinforcement learning (RL) learns control policies through experience, making it well-suited for highly nonlinear systems. However, a key limitation of standard RL is its reliance on online data collection, which can be expensive and time-consuming. Another major challenge is the difficulty of enforcing constraints, making it hard to guarantee stability and safety.

Control Barrier Functions (CBFs) extend the concept of stability by ensuring that a robot always remains within a predefined safe region. Integrating CBFs with learning-based control policies presents a promising solution to the safety limitations of conventional RL, especially in high-risk environments where failures can lead to severe consequences.

Guaranteeing safety under large environmental disturbances remains a challenge, particularly in unseen (out-of-distribution, OOD) scenarios. To address this, we also investigate methods for detecting and handling OOD data effectively. Enhancing overall stability not only expands the operational range of robots but also paves the way for broader applications in system automation.



--------
Generalizability
{: .fs-6 }

Learning-based modeling and control are valid only within the distribution of the acquired data, limiting their applicability to a single robot and a specific task. To ensure that a learned model remains effective across all possible scenarios, it is crucial to develop methods for acquiring data that comprehensively cover the entire operational range.

A promising approach is the use of foundation models, which have recently gained attention in the robotics and AI communities. These models, trained on vast datasets, can generate reasonable solutions even for problems they have not been explicitly trained on. In robot control, researchers are exploring the use of foundation models trained on large-scale datasets of various mobile robots and manipulators to control previously unseen platforms.

However, for non-standard robotic platforms, obtaining sufficient data to construct a foundation model remains a challenge. Furthermore, it is difficult to precisely define the boundaries of their applicability. Research on developing models that inherently understand and generalize fundamental physical properties across diverse robotic systems is significant, as it contributes to a broader understanding of robotics. In addition to foundation models, studying meta-learning techniques to enable rapid adaptation of learned models will play a crucial role in advancing practical robotic applications.
