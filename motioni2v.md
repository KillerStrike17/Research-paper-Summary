# Summary

## Motion- I2V:  
1. image-to-video results with large motion and viewpoint change.
2. supports users to more precisely control the motion trajectories and animated region with sparse trajectories (red curved arrow) and motion brush (purple mask).
3. supports zero-shot videoto-video translation.

### In Points
- uses I2V Models in 2 stages
    - Diffusion based motion field predictor
    - motion augmented temporal attension
- Result
    - Works well on medium brightness
- Problems in existing
    - I2V focused on Specific categories
    - I2V is limited in controllability
    - Narrow 1-D temporal attension lacks temporal consistency.
- Solution
    - predict plausible motion in form of pixel wise trajectory
        - Tune a Video Diffusion Model
        - Image and text as Input
        - Also train control net for motion predicting.
    - generate consistent animation

