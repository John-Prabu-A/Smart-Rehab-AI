# SmartRehab: AI-Driven Exercise Assessment and Live Feedback for Enhanced Recovery

![Project Status: Conceptual](https://img.shields.io/badge/status-conceptual-blue.svg)![AI for Good Innovate for Impact 2025](https://img.shields.io/badge/ITU%20AI%20for%20Good-Selected%20Project-brightgreen.svg)

**SmartRehab is a conceptual project selected for the ITU's "AI for Good Innovate for Impact 2025." This repository outlines our vision for an AI-powered system designed to revolutionize at-home physiotherapy by providing real-time, personalized feedback for rehabilitation exercises.**

## 📝 Project Vision

In many regions, there is a significant shortage of physiotherapists, making it difficult for patients with musculoskeletal disorders to receive the guidance they need. For instance, India has an average of only 0.36 physiotherapists per 10,000 people. This digital divide can hinder recovery, lead to improper exercise form, and make therapy ineffective.

Our proposed solution, SmartRehab, addresses this gap by creating an intelligent system that offers real-time corrective feedback and progress tracking for patients performing exercises at home. By leveraging accessible technology, we aim to democratize access to expert guidance, making at-home physiotherapy more affordable, scalable, and effective for everyone, regardless of their location or economic status.

## ✨ Key Features (Proposed)

*   **Real-time Pose Estimation**: Utilize state-of-the-art models like MediaPipe for accurate and fast human pose tracking.
*   **Instant Corrective Feedback**: Deliver live audio and visual cues to guide the user's form, ensuring exercises are performed correctly and safely.
*   **AI-Powered Assessment**: A custom Spatio-Temporal Graph Neural Network (STGCN) will be hosted on the cloud to evaluate exercise correctness and provide a detailed performance score.
*   **Personalized Experience**: The system will be designed to adapt feedback based on user-specific factors like age and historical performance, creating a tailored rehabilitation plan.
*   **Accessible & Cost-Effective**: The solution will be engineered to run on affordable hardware (like a Raspberry Pi) and connect to common displays, lowering the barrier to entry.

## 🛠️ Proposed System Architecture

The system will operate in a two-part process: local real-time feedback and cloud-based assessment.

1.  **Local Processing (On-device)**: A camera captures the user's movements. A low-cost computing device like a Raspberry Pi uses MediaPipe to extract pose keypoints and compares them against a reference exercise to provide immediate feedback.
2.  **Cloud Analysis (Post-Exercise)**: After the session, the collected pose data is sent to the cloud. Our ST-GCN model will analyze the movements to generate a comprehensive performance report, helping users track their progress over time.

![System Overview](https://github.com/John-Prabu-A/Smart-Rehab-AI/blob/main/figures/dia1_itu_v5.png)
*Figure 1: An overview of the proposed system architecture.*

![Sequence Diagram](https://github.com/John-Prabu-A/Smart-Rehab-AI/blob/main/figures/sequence_diagram_itu_v8.drawio.png)
*Figure 2: Sequence diagram of the SmartRehab system's workflow.*

## 🧠 The Proposed AI Model

The core of our assessment engine will be a **Spatio-Temporal Graph Neural Network (ST-GCN)**, an ideal architecture for understanding the complex dynamics of human movement.

The model will be trained using a **triplet loss** function to effectively distinguish between correctly and incorrectly performed exercises. This method will help create a robust model that can generalize well to different users. We plan to use public datasets like the **UI-PRMD** for initial training and fine-tuning.

![ST-GCN Model](https://github.com/John-Prabu-A/Smart-Rehab-AI/blob/main/figures/itu_dia2_v5.png)
*Figure 3: Schematics of the proposed ST-GCN Model for learning exercise correctness.*

## 🚀 Project Roadmap

As this project is in its inception stage, our immediate focus is on research, development, and building the foundational prototype.

1.  **Phase 1: Core Technology Development**: Develop the pose estimation and real-time feedback module on the Raspberry Pi.
2.  **Phase 2: AI Model Training**: Build, train, and validate the STGCN model for exercise assessment in a cloud environment.
3.  **Phase 3: Integration & Prototyping**: Integrate the local and cloud components into a functional end-to-end system.
4.  **Phase 4: Pilot Testing**: Deploy the system for testing in the Media Research Laboratory at our university, followed by trials in a typical home environment.

## 🔮 Future Work

Beyond the core system, we envision several enhancements:

*   **3D Sensing**: To overcome issues of self-occlusion in 2D video, we plan to explore 3D sensing technologies like Microsoft Kinect for more robust movement analysis.
*   **Expanded Language Support**: We aim to add support for multiple regional languages to maximize accessibility for non-English-speaking users.

## 👥 Team & Acknowledgments

This project is a proud initiative of Anna University, Chennai, and has been recognized by the ITU for its potential social impact.

*   **Dr. Dhananjay Kumar**: [dhananjay@annauniv.edu](mailto:dhananjay@annauniv.edu)
*   **B. Naren Karthikeyan**: [oraclenaren2004@gmail.com](mailto:oraclenaren2004@gmail.com)
*   **A. John Prabu**: [johnprabu0702@gmail.com](mailto:johnprabu0702@gmail.com)

## 📄 License

This project will be licensed under the MIT License. See the `LICENSE` file for details once the project's codebase is established.
