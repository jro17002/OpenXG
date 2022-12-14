
# Open XG 

A open source project to develop live xG prediction models 
from photo and video input using Computer Vision. 

<details open>
<summary> <font size = 4> Preprocessing </font> </summary>
<br>
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

Luckily we have standarized anchors that we can use to transform our photos to commonly align with each other. We will use the 6-yard box (and possibly the 16-yard box as well) to transform on the xy plane, we are unconcerned about the z-axis at the moment.

<center>
<table><tr>
<td> <img src="./visualizations/anchor_pts_vis.png" alt="Drawing" style="height: 250px;"/> 
    <center> 
            <p> Base Image, with Anchor Points </p> 
    </center>
</td>
<td> <img src="./visualizations/input_pts_vis.PNG" alt="Drawing" style="height: 250px;"/> 
    <center> 
            <p> Input Image, with Input Points </p> 
    </center>
</td>
</tr></table>
</center>

After using the input and anchor points we get the following transformed image which is now we can now derive theta from.
<center>
<table><tr>
<td> <img src="./visualizations/anchor_pts_vis.png" alt="Drawing" style="height: 250px;"/> 
    <center> 
            <p> Anchor Image </p> 
    </center>
</td>
<td> <img src="./visualizations/transform_vis.png" alt="Drawing" style="height: 250px;"/> 
    <center> 
            <p> Transformed Image </p> 
    </center>
</td>
</tr></table>
</center>

Full transform visualization:
<center>
<img src='./visualizations/transform_vis.gif' width= '720'/>
</center>

See [perspective_preprocessing.ipynb](https://github.com/jro17002/OpenXG/blob/master/perspective_preprocessing.ipynb) for code.

</details>

<br> 

## Authors

- [@jro17002](https://www.github.com/jro17002)


## Acknowledgements

 - [What are expected goals (xG)? ](https://theanalyst.com/na/2021/07/what-are-expected-goals-xg/)
 - [How to Build An Expected Goals Model](https://www.youtube.com/watch?v=bpjLyFyLlXs&t=1201s)

