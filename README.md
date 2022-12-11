<strong> Training, export and test <a href="https://github.com/Gainward777/yolov5">Customized YOLOv5</a> 
<br>
<strong> Dataset <a href="https://universe.roboflow.com/pricecarddemo/numbers-sdsol">NUMBERS Computer Vision</a>
<br>
The result can be seen:
<a href="https://github.com/Gainward777/Pricer">Android App</a> </strong>

The dataset used in this work did not contain small numbers usually denoting parts of the whole. <br>
To isolate them from the total mass, you can use the calculation of the area of the predicted bonding boxes. <br>
To do this, in the new_sorter function of the model, you need to add something like that:
<pre>
x1 = non_max[:, 0]
y1 = non_max[:, 1]
x2 = non_max[:, 2]
y2 = non_max[:, 3] 

areas = (x2 - x1) * (y2 - y1)
</pre>
Further, you can work with the corresponding values both in the function itself and on the device.

