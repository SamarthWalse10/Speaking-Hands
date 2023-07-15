# Speaking-Hands
The project's primary coding is carried out using Arduino IDE
To calibrate and modify the outputs of the flex sensors to suit our needs,
we have developed our own library (FlexSensor.h). There are primarily two operating
modes:
<p><b> i. Training Mode</b></p>
<p><b> ii. Testing Mode</b></p>
Some labelled sample datapoints will be stored in the SD card module 
during the training mode. The data points will be a 16x200 1D flattened 
array. The user's hand motions in testing mode will produce a new datapoint, a 
16x200 sized 1D flattened array. All the previously stored data points on the 
SD card will be compared to this new data point. The root mean squared error (RMSE) 
will be used as the foundation for comparison. The testing data point will 
be deemed a match if it has the lowest root mean squared error in relation to the 
new data point and meets a minimal threshold criterion. The bluetooth 
module will transmit the mp3/mp4 file associated with the match to the 
speaker box, and the amplified signal will then be broadcast through the 
speaker.
<br/><br/>
<p align="center">
  <img width="480" height="433.5" src="https://github.com/SamarthWalse10/Speaking-Hands/assets/125689593/016972df-e8cd-45ec-a981-bb2a34041050"/>
</p>
