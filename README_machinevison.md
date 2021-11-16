## About the frontmask vanisher

- Author: Lou Yuefeng
- Revised: Lou Yuefeng
- Date: 2021-11-15
- Version: 1.0.0
- Abstract: A rough idea about the task with regard to sign detection
### Functions Considered:
	Firstly the **cv.matchtemplate()/BFMatcher.match()** can compare the two objects in straightforward way, while the triangel in the task may be inclined or distorded, so such method might not work so well.
	Then **findHomography()** function compare the features with more advanced mathod taking 3D factors into account, could work in the task.
	The **machine learning** functions like knn or yolov5 form my perspective works best, I tagged some pictures acquired in the video, but haven't train it yet.
	The **cv_bridge()** function gets video stream frame by frame transported from camera.

