<h1>Inverse Kinematics Solution using Neural Networks</h1>


<h2>Description</h2>
This project utilizes the dataset of an ABB IRB120 six-degree-of-freedom (DOF) robot arm from Kaggle. It was generated from various end-effectors’ positions using forward kinematics (FK), which then became the input used to feed into the neural network models. And the derived joint angles were mapped to the end-effectors’ position. Usually, resolving the inverse kinematics (IK) problem with conventional numerical methods presents complex and non-linear challenges owing to the requirement of timeliness, precision, and accuracy. Meanwhile, neural network applications to Inverse Kinematics (IK) problems show faster methods of providing IK solutions.  And so, this research examines different performance capabilities of three neural network models when applied to IK datasets. The datasets were trained individually on Long-Short Term Memory (LSTM) neural network, Feed-forward Neural Network (FNN), and Recurrent Neural Network (RNN) using Keras on TensorFlow. During performance analysis, the LSTM model proved to be better in predictions as it gave the smallest joint error in the Cartesian workspace.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
