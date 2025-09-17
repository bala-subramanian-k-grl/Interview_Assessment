# Software Engineer Interview Assignment

## Objective
This assignment evaluates your ability to **analyze software systems, document architectures, and suggest meaningful extensions**. You will review real-world repositories, create structured documentation in Markdown, and explain flows with diagrams where needed.

---

## Instructions

1. **Format**
   - All deliverables must be in **Markdown (.md)** format.
   - Use **clear headings, subheadings, and bullet points**.
   - Include **architecture diagrams** (Mermaid) to explain flows and components.

2. **Repositories**
   - Zephyr RTOS: [https://github.com/zephyrproject-rtos/zephyr](https://github.com/zephyrproject-rtos/zephyr)  
   - Attendance Repository: [https://github.com/bala-subramanian-engineer/Face-Recognition-System/tree/main](https://github.com/bala-subramanian-engineer/Face-Recognition-System/tree/main)

   - Motion Detection (smolVLM): [https://github.com/ngxson/smolvlm-realtime-webcam](https://github.com/ngxson/smolvlm-realtime-webcam)

3. **Tasks**
   ### Task 1 – Zephyr RTOS
   - Analyze the **Zephyr RTOS** repository.  
   - Deliverable: Write a **technical architecture document** in Markdown covering:  
     - Core components (kernel, subsystems, drivers, networking, build system).  
     - Component interactions and data/control flows.  
     - High-level deployment/usage view.  
   - Include an **architecture diagram** to summarize the system.

   ### Task 2 – Motion Detection with smolVLM
   - Analyze the **smolVLM realtime webcam repo**.  
   - Deliverable: Document in Markdown:  
     - **Core architecture** of the repo.  
     - How **motion detection using Python and smolVLM model** works.  
     - An **architecture diagram** to illustrate components and flow.  
     - Explain how this could be **extended or integrated** with the attendance repo.

    ### Task 3 – Extend Attendance Repo with Gesture Recognition

    ### Objective
    Extend the current **Face Recognition Attendance System** by adding **Hand Gesture Detection** features.

    The system should be able to:
    1. Detect **if a hand is present** in the camera feed.
    2. Identify **which hand it is** (Left Hand or Right Hand).
    3. Count the **number of fingers** being shown.
    4. Recognize **specific gestures** like:
    - 👍 Thumbs Up
    - 👎 Thumbs Down

    ---

    ### Inputs & Outputs

    ### Input
    - **Live video frames** from the Camera (same input source as face recognition).
    - Frames will contain **hands** with different poses and gestures.

    ### Output
    - **Hand Presence**: "Hand Detected" or "No Hand".
    - **Hand Side**: "Left Hand" or "Right Hand".
    - **Finger Count**: Number of fingers shown (0–5).
    - **Gesture Type**: "Thumbs Up", "Thumbs Down", or "Other".

    ---

    ### Tasks Breakdown

    ### 1. Hand Detection
    - Use a library like **OpenCV** or **MediaPipe Hands**.
    - Detect bounding boxes around hands in each frame.
    - Output: `Hand Detected` + bounding box coordinates.

    ### 2. Hand Side Identification (Left / Right)
    - From detected hand landmarks, decide if it is the **left hand** or **right hand**.
    - Output: `"Left Hand"` or `"Right Hand"`.

    ### 3. Finger Counting
    - Based on hand landmarks:
    - Check which fingers are **open** or **closed**.
    - Count the total number of open fingers.
    - Output: `"Finger Count: N"`.

    ### 4. Gesture Recognition
    - Define rules for common gestures:
    - **Thumbs Up**: Thumb extended, all other fingers folded.
    - **Thumbs Down**: Thumb down, all other fingers folded.
    - Output: `"Gesture: Thumbs Up"` or `"Gesture: Thumbs Down"`.

    ---

    ### Storage & Logging

    - Extend the **Logger** module to also record:
    - Gesture detection events.
    - Performance details (CPU, memory usage).


 ### 4. AI Tool Usage
   - For repo analysis, you must use the following **prompt** (in any AI tool of your choice):

     ```
     As a technical expert, analyze this codebase and provide a clear project overview:
     - Core Components: Describe the major components or modules, their responsibilities, and any key classes or functions they contain. Note any relevant design patterns or architectural approaches.
     - Component Interactions: Explain how the components interact, including data and control flow, communication methods, and any APIs or interfaces used. Highlight use of dependency injection or service patterns if applicable.
     - Deployment Architecture: Summarize the deployment setup, including build steps, external dependencies, required environments (e.g., dev, staging, prod), and infrastructure or containerization details.
     - Runtime Behavior: Describe how the application initializes, handles requests and responses, runs business workflows, and manages errors or background tasks.
     ```

### 5. Submission 
   - Upload your code all your architecture diagrams as `".md"` in GitHub .  

### 6. Evaluation Criteria
   - Clarity and completeness of documentation.  
   - Accuracy in describing architectures, flows, and behaviors.  
   - Effective use of diagrams to explain complex concepts.  
   - Quality of extension proposals.  
   - Overall presentation and readability.  



---


