![alt text](https://github.com/ajastr/design-space-exploration-with-vae/blob/main/WEB%20APP/ReadmePicture.jpg?raw=true)


Design space exploration with VAE step by step:

![alt text](https://github.com/ajastr/design-space-exploration-with-vae/blob/main/MODEL/WofklowPicture.png)
1. Create parametric model

    Example model in the folder "parametric model" was created in Grasshopper for Rhino.

2. Run simulation. 

    Structural simulation was run using Karamba plug-in for Grasshopper.

3. Create dataset 

    Dataset has been created by random generation of parameters. Parameters and simulation results are saved to a .csv file
    
4. Train VAE

    Conditional Variational AutoEncoder example notebook was prepared using keras and following references:
    
    https://blog.keras.io/building-autoencoders-in-keras.html
    
    https://keras.io/examples/generative/vae/
    
    https://wiseodd.github.io/techblog/2016/12/17/conditional-vae/

5. Generate samples from the latent space using decoder

    Genration using saved decoder model inside grasshopper can be done with Hops plug-in.
    
6. Create performance map

    Running simulations for generated samples enables to create a map of latent space encodings for each performance condition.
    The map for performance condition p=0 should generate best performing samples, increased p value should correspond to geometries with worse performance.
    
7. Interactive design space exploration

    Grasshopper script enables "walking" on the perofmance map and exploring corresponding geometries.
    compute.Rhino3d.appserver can be used to share the script on the web and make the exploration accessible without any software
