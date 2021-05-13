# Technical Animation (Spring 2021) Blog

### FINAL PROJECT PRESENTATIONS: TBD

### More Learning (5/5)

For our final lecture, we wrapped up discussing on learning with a paper that achieved simulating high jumps, which even set out to achieve a new form of high jump method (which I found to be very ambitious and intriguing). The jumps looked really painful, the characters seem to just crumple up and land headfirst into the matt! But Prof. Pollard pointed out that the characters were likely unconstrained/unrestrained after the leap over the pole and subsequent fall. I wonder how complex it would be to extend the learning model to simulate that follow-through to completion.

### Learning I (5/3)

The discussion on learning today was on multi-legged locomofation with learned centroidal dynamics based on a predictive model, which receives patterns for some duration of time and then spits out full-body motion segments to be used in the future of the character's motion. It was really intriguing to see the gamut of motions that can be achieved using such a powerful and also highly efficient model (thanks to adaptive motion synthesis).

### Character Simulation (4/28)

Today we studied locomotion control (state machine-based control), and looked at several papers that investigate this for both bipeds and animal-like figures. Jessica Hodgins' paper on automating computer character animation was introduced as a formative approach in this space: it achieved physical realism by using standard physically-based simulation (using masses, springs, pendulums) and task control to guide motion characteristics, like speed/direction/gait, both offered at a high level (i.e. not hand-animated). We then moved on to subsequent papers that explored biped locomotion control (particularly that of bipedal humans) through use of motion capture data and feedback-error learning and modeling. At the end of class, we discussed more recent advancements in this area, specifically applying motion graphs and modern machine learning techniques like reinforcement learning. For example, we discussed Facebook Research's clustered learned controller (experts) system, which utilizes learning from motion graphs constructed from motion capture data.

### The Human Body (4/26)

We discussed modeling the general human body, starting off with hands. We first looked at Jernej Barbic's paper on hand modeling and simulation using MRI. After watching a few demos of the system in class, I and several others noticed that while the motion system was fairly robust, the hands looked fairly fleshy and exhibited uncanny deformability. For example, I noted that in the finger pinching demo of the skeleton mesh kinematic rig, the creases at the base of the fingers (where the fingers meet the palm) experienced faint deformation, whereas more skin/flesh would fold over in a real hand demo. However, further examples of the paper's soft tissue Finite Element Method simulation rig exhibited more realistic behavior. Overall I found this paper to be really unique, since it combines MRI imaging techniques to gather the skeleton rigs as well as more "hands-on" (pun-intended) traditional methods of molding hands in plastic to obtain 3D-scanned meshes. 

The other papers covered today spanned the area of human shape modeling, posing, and skinning, in addition to a (very recent) paper that capturing clothing in body models. This last paper was fairly interesting to me because it focused on providing an approachable method to generate realistic (pose-aware) avatars for clothing movement/deformation by using 3D scans, which can be animated using existing models. 

### Faces (4/21)

Today we discussed faces. I've seen Yaser Sheikh's presentation which uses multiview capture before (he gave a talk during a Facebook career event day); the demonstrations are pretty realistic, but nevertheless (or perhaps, because of how realistic it is) unsettling... A lot of methods for realistic face animation is grounded in gathering a lot of tracking data (especially eye tracking), or using fairly complex machine-learning (specifically natural language processing for lips and speech), so it was interesting to see the the multidisplinary approaches the other papers took today. A second paper of Yaser Sheikh's was also presented on that front ("An Integrated Eye and Face Model for Photorealistic Facial Animation"), using Facebook VR headsets to capture eye motions and track gaze. As expected, Facebook Reality Labs surely do have amazing resources...

### Paper Presentations IV + More Deformables (4/19)

The remaining paper presentation were covered today in class. I've been looking forward to Anne's presentation on the anisotropic material-point method used to simulate food damage mechanics, since her paper was one of my choices for the presentation. Though the results wer eparticularly compelling for sinew-like foods (i.e. string cheese, meat), I found the orange tearing to be quite uncanny, since I would typically associate oranges to be more pistules/pulpy (there are granules rather than straggly tears).

We then continued discussion on deformables. I found Prof. Pollard's paper to be quite interesting, as it included discussion on executing simulations on the GPU and I've been historically interested in learning more about parallel workloads and performance optimizations. It got me thinking about how parallelized collision detection algorithms can alleviate some of the more sequential woes of iterative simulations. The starfish and Michelin-man(? think that's what the character is called, otherwise Marshmallow man) were were also extremly convincing.

### Deformables (4/14)

Today we started our discussion on deformables, specifically covering the As-Rigid-As-Possible and Finite Element techniques. For the former, I liked the paper on the Teddy sketching interface; it seems almost magical how one can extract a dynamic deformable 3D skeleton just from a set of simple 2D strokes. For the latter, we saw a nice constrast between simulating brittle fractions and goop for the latter.

### Paper Presentations III (4/12)

Today's paper sessions consisted of a lot of fluid simulation papers! The paper I liked the most was Alice's presentation on an octree liquid simulator, which uses an octree for Poisson discretization and Movling Least Squares for the octree interpolation. Though the details were fairly complex, as someone interested in geometry queries/collisions and performance acceleration (on the hardware level), I was intrigued in how they achieved an extremely detailed level of discretizations that was still but also blazingly fast. The results were also extremely aesthetic.

### More Fluids (4/7)

Today we continued to learn about more techniques to improve Eulerian solvers for fluids, particularly focusing on improving the projection step to minimize dissipation (conserve mass/energy). The PIC/FlIP/APIC methods illustrated both the issues and potential pros that using grids and/or going back and forth in problem representation of particles can lead to. The Smoothed Particle Hydrodynamics (SPH) method sounds fairly promising and efficient to simulate breaking/splashing waves.

### BREAK DAY - NO CLASSES (4/5) 

### Fluids (3/31)

We learned about simulating fluids based on the Navier-Stokes equations, and in particular, covered papers that investigated making solvers that were fast and stable. 
I read Stam's paper for implementing a fluid dynamics solver when I was formulating my final project idea. I liked that the approach requires utilizes a lot of grid/field-based and linear system logic; for example, Gauss-Seidel relaxation is used to achieve stability in the density diffusion step, and the Poisson equation is used for the projection step. Though the basic implementation for simulating water is fairly cool, I think the applications for smoke and mist particles is pretty interesting, and this paper has pretty convincing examples of smoke diffusion. As an ex-TA, I think this grid-based approach using a parallel framework/on the GPU would be a classic 15-418 (Parallel Computer Architecture) project idea.

### Miniproject 2 Presentations (3/29)

The other half of the class presented their work on Mini-Project 2. Most of us ended up doing the mass-spring option (#1), as I expected. It was interesting to see the variety of platforms people used; most people got their UI/codebases from other sources (mine as well). I was especially intrigued by Max and Alice's choice of platforms. Alice got her codebase off of one of Berkeley's graphics course websites; it seems like that codebase made it really easy to handle collisions, and I am jealous that the UI was so intuitive to use, as I had to build mine from scratch... 

Max's demo of cloth collisions (even self-collisions, I believe) in Scotty3D was super impressive. Seeing both of their work inspires me to continue exploring collisions beyond Mini-Project 2; maybe I'll find their work useful for my final project.

### Final Project Pitches II (3/24)

The couple remaining students (including myself) presented their final project ideas. I presented my final project idea for simulating jello as a 3D mass-spring system and exploring collision-handling as an extension of my mini-project 2.

After the final pitches, the discussion on collision was wrapped up with a paper on signed distance field collision, and then we started covering character simulation. Today's papers were a preview for optimization/trajectory-based simulations. I liked looking at the results of Prof. Pollard's paper on optimizing complex human motions, and it's really fascinating to see that optimization problems can be solved to handle such intricate movements. The joke ray-tracing Jell-o paper covered at the end of class was pretty amusing as well. The paper sounds very ambitious; I certainly will not be utilizing Schrödinger's wave equation or supercomputers to simulate my jello, although it would be interesting to investigate... if I had more resources to quantum computing.

### Final Project Pitches I (3/22)

Today most people presented their project pitches. I was impressed by the variety of topics. Some of my friends picked pretty ambitious paper ideas, like Hesper's simplicial fluid simulator (the algorithm of which is extremely complex). I found Anne's MPM proposal for investigating jello/snow simulation behavior to be the most interesting, since I'm working on a jello simulation idea for my final project. Prior to class, we had talked about some resources for MPM simulations, since I'm also working on a jello simulation idea for my final project, using the traditional mass-spring model (extending project 2). Since we are taking two different approaches to achieving jello-like behavior, I'm excited to see if we can simulate similar collisions/behaviors - it would be a nice side-by-side comparison of the methods!

### Paper Presentations II (3/17)

I gave my presentation on "A Safe and Fast Repulsion Method for GPU-Based Cloth Self-Collisions". I think my paper was pretty interesting: the intuition behind the constraints chosen were fairly straightforward, and I liked how they proposed an adaptive remeshing scheme to bolster their methodology. With my background in GPUs, I particularly appreciated how they gave a description of writing a kernel to perform their iterative two-phase collision handling approach.

I also liked Max's presentation on position based dynamics!

### Rigid Bodies and Contact (3/15)

Today we discussed a variety of techniques in contact and collision detection: impulse-based, penalty-based, and constrain-based. Earlier in class we also briefly mentioned Andrew Witkin and David Baraff's course notes for physically-Based Modeling, which I've come across a handful of times in related work I've researched while coming up with what I should do for the final course project (modeling jello). I will probably continue to reference it while I do mini-project 2 and refine my final project idea.

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