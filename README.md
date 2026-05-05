<h1>Inverse Kinematics Solution using Neural Networks</h1>


<h2>Description</h2>
This project utilizes the dataset of an ABB IRB120 six-degree-of-freedom (6DOF) robot arm from Kaggle. It was generated from various end-effectors’ positions using forward kinematics (FK), which then became the input used to feed into the neural network models. And the derived joint angles were mapped to the end-effectors’ position. Usually, resolving the inverse kinematics (IK) problem with conventional numerical methods presents complex and non-linear challenges owing to the requirement of timeliness, precision, and accuracy. Meanwhile, neural network applications to Inverse Kinematics (IK) problems show faster methods of providing IK solutions.  And so, this research examines different performance capabilities of three neural network models when applied to IK datasets. The datasets were trained individually on Long-Short Term Memory (LSTM) neural network, Feed-forward Neural Network (FNN), and Recurrent Neural Network (RNN) using Keras on TensorFlow. During performance analysis, the LSTM model proved to be better in predictions as it gave the smallest joint error in the Cartesian workspace.
<br />


<h2>Hardware</h2>

<p align="center">
ABB IRB120 <br/>
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
Position and Orientation of a 6DoF Robot Arm <br/>
<img src="https://i.postimg.cc/0Q9sP9jz/6dof-robot-arm-schematic.png" height="50%" width="30%" alt="Disk Sanitization Steps"/>
<br />

<b>(2)</b>
 <b>Use an IDE (Google Colab) to load and train the dataset individually on the LSTM, FNN, and RNN models with TensorFlow (Keras) learning frameworks. </b>
 - <b>Inverse Kinematics (IK) - For a 6 DOF robot arm, IK is used to describe how the specified position and orientation of the end-effector is gotten from an established joint angle in a 3D space. The transformation equation of a 6 DOF can be written as:</b>
<b><img src="https://i.postimg.cc/x1Ddn7Z3/Screenshot-2026-05-05-102143.png" height="45%" width="25%" alt="Disk Sanitization Steps"/></b>

 - <b>Neural Networks - Ideally, neural networks fit best in resolving non-linear equations, particularly IK equations. This is because they are learning-based regression models that work well in mapping the robots’ end-effector’s position and orientation to its joint angles. Having generated the training data through forward kinematics, the input or features, which is the end-effector’s pose, is mapped in the neural network to the output or target, which are the joint angles.:</b>

   <b><img src="https://i.postimg.cc/0j77ym9h/Screenshot-2026-05-05-102240.png" height="60%" width="40%" alt="Disk Sanitization Steps"/></b>

<p align="center">
Mathematical Model for a Neuron <br/>
<img src="https://i.postimg.cc/fbrwJrLX/Picture1.png" height="30%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<b>(3)</b>
<b>Perform the validation on the individual trained models to ascertain the results on mean square error (MSE), mean absolute error (MAE), R2 score, and end-effector error (mean and max.).</b>
- <b>Mean Squared Error (MSE) – This measures the average square difference between the predicted and the true joint angles in the dataset and returns a single number or a score. Meanwhile, in supervised learning, the goal of training with MSE is to reduce loss.</b>

   <b><img src="https://i.postimg.cc/DfqPPkTS/Screenshot-2026-05-05-104917.png" height="10%" width="20%" alt="Disk Sanitization Steps"/></b>

- <b>Mean Average Error (MAE) – This measures the average size of joint angle errors in each number of predictions.</b>

   <b><img src="https://i.postimg.cc/VL91w6P4/Screenshot-2026-05-05-104950.png" height="10%" width="20%" alt="Disk Sanitization Steps"/></b>

- <b>R2 – This is a measure of best fit on the model. It measures how well the predicted joint angles correctly align with the true joint angles.</b>

   <b><img src="https://i.postimg.cc/RCRXz5bL/Screenshot-2026-05-05-105008.png" height="10%" width="20%" alt="Disk Sanitization Steps"/></b>

- <b>End-effector error – This is a measure of the predicted joint angle’s deviation of the end-effector in space from its desired pose.</b>

   <b><img src="https://i.postimg.cc/V6N5rtmW/Screenshot-2026-05-05-105036.png" height="10%" width="20%" alt="Disk Sanitization Steps"/></b>

<b>The dataset used to train each of these models contains 15,000 samples of end-effectors (x, y, z) and joint angles (θ1, θ2, θ3, θ4, θ5, θe). After training the three models, their test outcomes and loss curves are presented in the table and figures below to compare and establish the model that fits better with the IK dataset. </b>


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
