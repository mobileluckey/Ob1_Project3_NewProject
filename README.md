\# Project 3: AI Motion Detection + IoT Alert System  

\### Objective 1 – Create, Analyze, and Integrate AI \& IoT Systems



This project uses a webcam, computer vision, and MQTT to create a simulated IoT motion detection system with an AI-style analysis layer.



\## Project Overview



\- A \*\*Python motion detector\*\* uses OpenCV to monitor a video stream (webcam or video file).

\- When motion is detected, it publishes a JSON event message to a \*\*HiveMQ Cloud\*\* MQTT topic.

\- A separate \*\*AI subscriber\*\* script listens for those messages, keeps a rolling window of recent events, and classifies the environment as:

&nbsp; - `QUIET`

&nbsp; - `NORMAL`

&nbsp; - `HIGH ACTIVITY`

\- Events are logged to a CSV file for future machine learning.



This shows how computer vision (AI), messaging (MQTT), and IoT-style event handling can work together as a complete system.



\## Planned Structure



```text

Ob1\_Project3\_NewProject/

│

├── README.md

├── .gitignore

├── src/

│   ├── motion\_publisher.py        # Detect motion and publish MQTT events

│   └── motion\_ai\_subscriber.py    # Analyze events and classify activity level

└── images/

&nbsp;   └── architecture.png           # Architecture diagram (to be added)



