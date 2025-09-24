**Wake-Word Detection on Embedded Hardware**

This project implements an always-on wake-word detection system optimized for embedded hardware using TensorFlow Lite for Microcontrollers (TFLM). It enables real-time, low-power voice command recognition for controlling an LED via multi-word voice input.

**Features**

Custom Sine-Prediction Model: Designed and trained from scratch to serve as a base model before extending to wake-word tasks.
TensorFlow Lite Conversion: Trained TensorFlow models converted to .tflite format for embedded deployment.
Optimization & Trade-offs: Analyzed model memory footprint, inference latency, and accuracy to balance performance on microcontrollers.
Always-On Wake-Word Detection: Real-time keyword spotting deployed on Arduino Nano 33 BLE Sense.
Multi-Word Recognition: Supports multiple wake-words to trigger different actions.
Voice-Controlled LED Demo: On-board LED turns on/off based on detected wake-word.

**Hardware & Software**

Hardware
Arduino Nano 33 BLE Sense (with onboard microphone & ARM Cortex-M4F processor)
LED (onboard or external)
Software / Tools
Python 3.x
TensorFlow / TensorFlow Lite
TensorFlow Lite for Microcontrollers (TFLM)
Arduino IDE or PlatformIO

**Setup & Deployment**

Train Model
Train sine-prediction and wake-word classification models in Python using TensorFlow.
Export model to .tflite format.
Convert to TFLite for Microcontrollers
xxd -i model.tflite > model_data.cc
Embed the model into Arduino firmware.
Deploy on Arduino
Open Arduino IDE.
Install Arduino_TensorFlowLite library.
Upload code with model_data.cc integrated.
Test Wake-Word Detection
Speak wake-words (e.g., "On", "Off").
Observe LED control in real-time.

**Performance Analysis**

Memory Usage: Optimized for <256KB RAM footprint.
Inference Delay: <100 ms per audio frame.
Accuracy: Balanced for embedded constraints while maintaining reliable recognition.


**Applications**

Voice-controlled IoT devices
Smart assistants on resource-constrained hardware
Always-on low-power wake-word detection

**References**

TensorFlow Lite for Microcontrollers
Arduino Nano 33 BLE Sense# Embedded-Machine-Learning
