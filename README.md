<h1>Inverse Kinematics Solution using Neural Networks</h1>


<h2>Description</h2>
This project utilizes the dataset of an ABB IRB120 six-degree-of-freedom (6DOF) robot arm from Kaggle. It was generated from various end-effectors’ positions using forward kinematics (FK), which then became the input used to feed into the neural network models. And the derived joint angles were mapped to the end-effectors’ position. Usually, resolving the inverse kinematics (IK) problem with conventional numerical methods presents complex and non-linear challenges owing to the requirement of timeliness, precision, and accuracy. Meanwhile, neural network applications to Inverse Kinematics (IK) problems show faster methods of providing IK solutions.  And so, this research examines different performance capabilities of three neural network models when applied to IK datasets. The datasets were trained individually on Long-Short Term Memory (LSTM) neural network, Feed-forward Neural Network (FNN), and Recurrent Neural Network (RNN) using Keras on TensorFlow. During performance analysis, the LSTM model proved to be better in predictions as it gave the smallest joint error in the Cartesian workspace.
<br />


<h2>Hardware</h2>

<p align="center">
ABB IRB120: <br/>
<img src="https://i.postimg.cc/tJRhHnFR/abb-irb-120-robotics.jpg" height="50%" width="30%" alt="Disk Sanitization Steps"/>
<br />
 

<h2>Languages and Utilities Used</h2>

- <b>Python</b> 
- <b>TensorFlow</b>

<h2>Environment</h2>

- <b>Google Colab</b>

<h2>Project walk-through:</h2>
<b>(1)</b>
 <b>Collect the numerical inverse kinematic dataset as a CSV file having joint angles and end-effector position for the ABB IRB120 six-DOF robot arm (targets and features). </b>

<p align="center">
Position and Orientation of a 6DoF Robot Arm: <br/>
<img src="https://i.postimg.cc/0Q9sP9jz/6dof-robot-arm-schematic.png" height="50%" width="30%" alt="Disk Sanitization Steps"/>
<br />

<b>Step 2</b>

- <b>Train the DQN model with the data collected using a well-structured set of hyperparameters</b>
- <b>Ensure the reward functions are continuously tuned to improve stability and convergence</b>

<p align="center">
DQN Training Network Architecture: <br/>
<img src="https://i.postimg.cc/TY2Y6qSN/Picture1.png" height="60%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<b>Step 3</b>

- <b>Perform testing to ensure that the robot learned the trajectory pathway and obstacle detection</b>
- <b>Evaluate the testing outcomes</b>

<p align="center">
Results - (a) Action-Distribution, (b) Sensor Over Time, (c) Robot Motion Trajectory: <br/>
<img src="https://i.postimg.cc/Hs2GTq54/Screenshot-2026-05-05-022659.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<br />


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
