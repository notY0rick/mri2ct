# mri2ct

This is my final project for COMPSCI 280: Computer Vision at the University of California, Berkeley.
The main task of the project is to train a model that is capable of converting a magnetic resonance image
(MRI) to a computed tomography (CT) scan. Conceptually like so:

![](https://scontent-sjc3-1.xx.fbcdn.net/v/t1.15752-9/359675407_1571982369993707_2709872867511280663_n.png?_nc_cat=109&cb=99be929b-3346023f&ccb=1-7&_nc_sid=ae9488&_nc_ohc=V8yqP75rjtYAX-vbCp_&_nc_ht=scontent-sjc3-1.xx&oh=03_AdQ3Hy4kvuoC9oLjSSQv2JNQl7br1W-d4uKX6flDFGDBRw&oe=64D1EE19)

On the left, we have the MRI scan, which is our input. In the middle column is the CT scan, which is our ground-truth.
On the right-most column is the synthetic CT (sCT) scan we hope the model is able to generate based on the input MRI.

Upon surveying several open-source models, I decided to train a pix2pix GAN to tackle this problem. Please refer to the `final_report.pdf`in this repository for more visualization examples
and other implementation details. Note: the `pix2pix.ipynb` is the notebook that includes the data processing
and handling and the actual training process of the pix2pix GAN. Overall, with very limited computing resources, the model
was able to produce fairly decent sCT's that resembled the ground-truth CT's.