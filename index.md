# Technical Animation (Spring 2021) Blog

### More Cloth (3/10)

We started class today by covering the "Robust Treatment of Collisions, Contact, and Friction for Cloth Animation", which was useful for understanding some key points for handling collisions (in particular, self-collisions). We also discuss limiting strain using momentum conserving impulses. The rest of the lecture, we covered other papers to handling tuning simulation parameters, which can be a sore point for spring mass systems. One of the papers that caught my eye was the "Adaptive Anisotropic Remeshing for Cloth Simulation", which uses an extreme intuitive anisotropic meshing scheme. The operations were reminiscent of the remeshing operations we implemented for MeshEdit in 15462, so it was quite interesting to see such intuitive operations had great efficacy in this paper's implementation; I think implementing the algorithms for this paper is very approachable, possibly in-scope for projects for this course. 

Looking at these options, I think I'm leaning towards implementing the spring-mass cloth simulator for Mini-Project 2, since we covered this technique in detail in class. 

### Simulation and Cloth (3/8)

Today we discussed the basics of a spring-mass cloth simulators and cloth integrators, which was all new to me (I've never made a simulation before). One of the papers discussed was one that presents a unified dynamics solver ("Nucleus: Towards a unified dynamics solver for computer graphics") by modeling mater as simplicial complexes, which I found to be pretty interesting. I think it would be helpful to read up on this paper to understand some of the design decisions/tradeoffs in using different integrators, which also happens to be an option I could explore for Mini-Project 2.

### Mini-Project 1 Presentations (3/3)

I enjoyed watching everyone's presentations! Anne and I gave our presentation on our mocap + keyframing efforts, and it prompted good discussion about the ease of use of euler vs. quaternion representations for these options, which other people found that they were also experiences issues with. I also really liked Alyssa's Blender visualizations for our CCD implementations.

### Learned Motion Matching (3/1)

We discussed the paper "Learned Motion Matching" by Holden et. al, an integral technique to modern animation systems using widely in gaming today. I was impressed by how intuitive motion matching is; smoothing the patchwork of clips is done by applying foot locking and IK, techniques that are also easy to understand. The learned motion matching system they propose is similarly just as intuitive, by using the idea of a motion matching search and combined features database (joining together matching feature database and extra features database), bu instead of actually using databases, using a series of neural networks to do search/predict combined features to emulate the search/lookup. The final results are indistinguishable from canonical motion matching systems, but with better scalability.

### Paper Presentations I (2/24)

I enjoyed everyone's paper presentations. I was especially impressed by the hand motion tracking paper pushed by Facebook Reality Labs, which targeted the difficulties of occlusion and self-contact in hand tracking. It was eerily impressive how their tracking algorithm combined with their physically-based model system robustly enabled pretty complex hand configurations. In addition, another student presented about optimizing stop-motion animation by replacing sequences with computer animation, which led to an interesting discussion of the artistic merits of the medium as a whole. 

### Rigging and Skinning (2/22)

Today we went over a survey of recent research on rigging and skinning, done mostly using advanced machine learning techniques. I liked implementing the simple version of linear blend skinning for 15462; it was interesting to learn more advanced techniques to combat the candy-wrapper effect using quaternions. Among the research papers for the day, I found the NeuroSkinning paper to be the most interesting, as it demonstrated several tests where there were noticeable cloth intersections without the method they used, and it got me thinking about how cloth collisions and skinning are not necessarily processed separately (i.e., they have impact on each other, and cloths sticking closer to the skin can suffer from issues related to bad skinning).

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