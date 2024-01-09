# YouTube Controller with Hand Signs Detection

![YouTube Controller](<image_path>/project_image.jpg)

## Overview

This project enables you to control YouTube playback using hand signs detected by a machine learning model. By recognizing specific hand gestures, the model triggers actions such as play, pause, volume increase, and volume decrease.

## Hand Signs

- **Play:** ![Play Sign]("C:\Users\joaqu\jupyter\YouTubeVideoController\ytcontroller\demo_signs\play.png")
- **Pause:** ![Pause Sign]("C:\Users\joaqu\jupyter\YouTubeVideoController\ytcontroller\demo_signs\pause.png")
- **Volume Up:** ![Volume Up Sign]("C:\Users\joaqu\jupyter\YouTubeVideoController\ytcontroller\demo_signs\up.png")
- **Volume Down:** ![Volume Down Sign]("C:\Users\joaqu\jupyter\YouTubeVideoController\ytcontroller\demo_signs\down.png")

## DEMO Video
![DEMO Video](https://www.youtube.com/watch?v=cby-C9cJ6YI&t=2s&ab_channel=joaquinestevez)

## Usage
1. Go to the "Model_creation.ipynb" file and to Section "10. YouTube Controller"

2. Run every cell of Section "10.1 Set up Pahts"

3. Run every cell of Section "10.2 Install Dependencies":

    - Make sure you run the verification script:
        ```python
        VERIFICATION_SCRIPT = os.path.join(paths['APIMODEL_PATH'], 'research', 'object_detection', 'builders', 'model_builder_tf2_test.py')
        # Verify Installation
        !python {VERIFICATION_SCRIPT}
        ```
        - Verify you get 'OK' at the very end. If not, install the needed dependencies.

    - If you get the ERROR "No Module named 'object_detection' when you import it, Restart your Kernel and run Section 10.1 Set up Paths again:
        ```python
        # If ERROR: "No module named "object_dections"" - IMPORTANT
        # Solution: Restart your Kernel and run again the 4 cells of Section 10.1
        ```
        ```python
        import object_dections
        ```

4. Run every cell of Section 10.3 Load and Run Program:

    - The last cell will open a YouTube window and activate the hand signs detection model.
    - You will need a webcam connected to your computer for this step.

## Important Notes:

    1. Make sure your camera is properly connected, and the environment has adequate lighting for accurate hand     signdetection.
    2. In case you are having issues with the camera, try changing "cap = cv2.VideoCapture(0)" by "cap = cv2.VideoCaptur(1)" in the last cell of Section 11. If the issue continues, try with 2, 3, or 4:

        ```python
        cap = cv2.VideoCapture(0) # change the '0' to '1', '2', '3', or '4'
        ```

5. Perform hand signs in front of your camera to control YouTube playback:

    Play: Show the "Play" hand sign.
    Pause: Show the "Pause" hand sign.
    Volume Up: Display the "Volume Up" hand sign.
    Volume Down: Present the "Volume Down" hand sign

4. Enjoy hands-free YouTube control!

5. Press 'q' when you want to finish the program
