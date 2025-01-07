# porosity-analysis-of-random-samples
Porosity Assessment in Randomly Generated 3D Savonnières Carbonate Samples

The high-value samples from random-3D-sample-generator were then analysed using open-source tools.

The first analysis was the porosity of each sample.
Aim was to quantify the absolute and effective porosities of each sample.

First tool used was the **BoneJ plugin** in Fiji-ImageJ
The following parameters were determined:
1. Pore shape - using the surface area to volume ratio
2. Connectivity - using the Euler characteristics
3. Pore Size Distribution - using the difference between the largest and smallest pores

The table of results is shown below. 
1st Column - Sample number and the coordinates for each sample
2nd Column - Number of voxels in largest connected pore space
3rd Column - Size of the smallest disconnected pore space
4th Column - The size of the median disconnected pore space
5th Column - The amount of pore space attributed to the largest interconnected space
6th Column - The pore distribution, with "W" denoting "Wide"

![image](https://github.com/user-attachments/assets/b7b76dbc-7386-4c32-9be7-1bf180da70fc)
![image](https://github.com/user-attachments/assets/595dc015-6d87-4e5b-8f2a-29036cfe3273)

Second tool used was **Python**

Total Porosity for each sample was calculated as follows in _porosity_calc_:
Total Porosity = Total Pore Voxels/Total Number of Voxels
The results for each sample were then plotted on a graph.
![porosity_otsu](https://github.com/user-attachments/assets/ae18b066-feaa-47a5-aaf2-9debdb8f9a2f)

Now comes the complex part.
I then set out to calculate the pore distribution along the length of each sample.
This is outlined in _pore_dis_
I then incorporated the coordinates of each sample.
This is outlined in _por_dis_coor_
I then combined each of these into a loop that calculated for each sample,
This is outlined in _por_dis_coor_comb_
Finally, I separated the original core sample into 3 regions.
From the top of the sample to 1500 micrometres was the "Top Region"
From 1500 to 3000 micrometres was the "Middle Region"
From 3000 to 4500 micrometres was the "Bottom Region"
I then calculated the average porosity and standard deviation for all the samples
by region and for the whole length
This is outlined in _pore_regions_

The output is shown below:
![image](https://github.com/user-attachments/assets/bca20034-ba8a-4802-9fcb-785aae70d9ef)
