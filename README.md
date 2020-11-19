# Summary

This is a quick attempt to calculate the pose of a single person in a video or image. All the notebooks in this repository has been focused on technique analysis of single cross country skiers. So, in this repository you will find 4 notebooks for different tasks and strategies to study the pose of the skier. So, in this repository you will find a notebook focused in calculate the pose of a single skier in a picture (ImagePose notebook). There is another notebook that perform the same strategy in the previous notebook, but it will calculate it for every frame of a video, and will record it (VideoPose notebook). However, this strategy tends to fail when skier is small in the frame (skier is far), so, with the help of a Yolov3, you can find every person in frames, and cut the image to zoom in skier (example of yolo detection in VideoPersonDetection notebook). In this way, you can find a solution in VideoOpenPose&PersonDetection notebook, that calculates the pose of skier doing zoom in skier when he is far, and without zoom when he is nearer. If Yolo decets more than one person, we will focus on the biggest one, because video it's supposed to be focused on the skier that is being studied.

Because of the quality of single frames, just for calculate the pose, you can choose an option to blurr vertical lines between frames with a gaussian filter (5,5) in the video notebooks. This blurring won't be in final result, and it uses to improve the result.

Here, we have an example of how it works for a video of a skier going uphill

![alt text](https://github.com/TuronLab/PoseDetection/blob/main/Example.gif "Example Video Pose detection")
