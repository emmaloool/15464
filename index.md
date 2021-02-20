# Technical Animation (Spring 2021) Blog

### Inverse Kinematics, Continued (2/17)

We recapped a previous discussion of inverse kinematics (the Jacobian tranpose, pseudoinverse, damped pseudoinverse, projections of other vectors into the nullspace), and eventually covered methods without using the Jacobian transpose. We first looked at a paper that adds priorities, and then another paper that parallelizes the classical approach, and finally a method that directly searches for the minimum. I really liked seeing the parallelization paper, since I've taken classes in computer architecture and like to see how systems and optimization techniques (obtaining better speedup, cache locality, etc.) can benefit fields in computer graphics.

### CLASS CANCELLED (2/15)

No notes for today!

### Inverse Kinematics + Mini-Project 1 (2/10)

Today, we reviewed more details about performing inverse kinematics, namely the differening ways that Jacobians can be calculated. This was an extension of our previous exposure to the Jacobian Tranpose in Computer Graphics; this review served to provide even better intuition than what we had in order to complete the Animation assignment for 462. 

We also briefly went over the details of the mini-project 1 assignment (and earlier in class, the paper session). I'll have to see which project I'll be doing, but I'm definitely interested in most of the options! I think the review of the Jacobian Transpose will make my life easier if I choose one of the Jacobian Transpose options for the project. 

### Motion Capture (2/8)

After taking a look at the state of the art in motion capture (ex., Yaser Sheikh's Panoptic Studio Dataset), we explored the topic of motion capture, by looking at a few examples and file formats, including CMU's Mocap Database; I found it particularly charming that the bone+joint hierarchy was labeled with anatomically correct names. The review also included a bit about how to transpose rotation matrices along the hierarchy.

### Introduction to Animation (2/3)

We were given a brief overview of the main topics we're covering this semester, including rigging and skinning, kinematics, motion, simulations (cloth, fluid), and body motion. Some of these concepts and even examples (i.e., the *Coco* and *Isle of Dogs* movie behind-the-scenes demos) were covered in 15-462: Computer Graphics lectures last semester. It was cool to see a more dedicated dive into the cutting-edge research in this course, and I look forward to building on top of the animation techniques I learned last semester, including forward and inverse kinematics.

### Course Overview (2/1)

We went over several new research publications in technical animation: the two that stood out to me the most were simulating boundary-aware waves and animating yarn-level cloth effects. I also liked the brief overview Prof. Pollard gave of her research on hand motion and modeling. I look forward to learning about general simulation and applications in this course, including cloth and light/fluid simulation (especially as it pertains to food)!