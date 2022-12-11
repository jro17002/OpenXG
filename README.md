
# Open XG

A open source project to develop live xG prediction models 
from photo and video input using Computer Vision. 


### Preprocessing

A component of any xG model is a player's position relative to the goal, intuitively we understand some positions are more difficult than others. I.e. A headon shot 10 yards out is easier than a shot 5 yards out but hugging the touchline. A easy way to quantify these positions is to derive a theta using the player's position and either goal posts. This theta can be used as a representation of an angle to goal. Simply, the larger the theta the better the chance. In order to derive a theta we must preprocess our images such that there is a sense of uniformity. We then can input keypoints to a standarized function and have that function return a theta.


<center>
<table><tr>
<td> <img src="./visualizations/theta_vis.png" alt="2D Representation" style="height: 250px;"/> 
        <center> 
                <p> 2D Representation </p> 
        </center>
</td>
<td> <img src="./visualizations/irl_theta_vis.png" alt="Real World Example" style="height: 250px;"/>
        <center> 
                <p> Real World Example </p> 
        </center>
</td>
</tr></table>
</center>




## Authors

- [@jro17002](https://www.github.com/jro17002)


## Acknowledgements

 - [What are expected goals (xG)? ](https://theanalyst.com/na/2021/07/what-are-expected-goals-xg/)
 - [How to Build An Expected Goals Model](https://www.youtube.com/watch?v=bpjLyFyLlXs&t=1201s)

