# Large style comparison 
In this section we compute a style dissimilarity score for a large dataset of characters.
![large table](https://github.com/fmerizzi/text_style_comparison/blob/main/large_table.png)
 
  - The labels on the table are relative to the letter's place of origin, so v is [1] from Venanson, s is [2] from Saint-Etienne, l is [3] from Luceram and i is [4] from Imperia. 
  - The inmages are resized to 512x512, lightly smoothed with a gaussian kernel and summarized to a single channel
 
The original source images are reported in : [source images](https://github.com/fmerizzi/text_style_comparison/tree/main/new_dataset)
 
 The code for producing these results is included in the repo by the name comparing_large_number_images.ipynb
 
# medieval writings style comparison and restoration  
Using gram matrices to compare calligraphy from medieval frescoes + deep image prior for text restoration. 

## style comparison 
For the style comparison we select six images all cointaining the letters "et", three come from "Cella di Macra" (c) and three from "Venanso" (v).

 - images are cut in a square format 
 - white balanced 
 - upscaled to 200x200 pixels 


e1c--------------------------------------------e2c--------------------------------------e3c


![e1c](https://github.com/fmerizzi/text_style_comparison/blob/main/sample_images/e1c.png)
![e2c](https://github.com/fmerizzi/text_style_comparison/blob/main/sample_images/e2c.png)
![e3c](https://github.com/fmerizzi/text_style_comparison/blob/main/sample_images/e3c.png)


e1v--------------------------------------------e2v--------------------------------------e3v


![e1v](https://github.com/fmerizzi/text_style_comparison/blob/main/sample_images/e1v.png)
![e2v](https://github.com/fmerizzi/text_style_comparison/blob/main/sample_images/e2v.png)
![e3v](https://github.com/fmerizzi/text_style_comparison/blob/main/sample_images/e3v.png)

We then compute dissimilarity scores within the two groups and against each other. 
The score is rounded to the the 2nd decimal value and multiplied by 100 for ease of readibility. 

**result table**


![table](https://github.com/fmerizzi/text_style_comparison/blob/main/Screenshot_20221015_185331.png)

**scores**


Venanso within group dissimilarity = 0.3866

Cella di Macra within group dissimilarity = 0.2966

Extra group dissimilarity = 0.3744

## Text Inpainting 
Inpainting test applied to letter "a" from Cella di Macra. Image is upscaled, white balanced, squared by expanding border content and smoothed with a gaussian blur. 
Deep image prior is used with the same configuration used for the frecoes. 

**inpainting with mask 1**


![e1v](https://github.com/fmerizzi/text_style_comparison/blob/main/text_inpainting/inpaintingA_mask1summary.png)


![e1v](https://github.com/fmerizzi/text_style_comparison/blob/main/text_inpainting/res_mask1.png)


**inpainting with mask 2**


![e1v](https://github.com/fmerizzi/text_style_comparison/blob/main/text_inpainting/inpaintingA_mask2summary.png)


![e1v](https://github.com/fmerizzi/text_style_comparison/blob/main/text_inpainting/res_mask2.png)


**inpainting with mask 3**


![e1v](https://github.com/fmerizzi/text_style_comparison/blob/main/text_inpainting/inpaintingA_mask3summary.png)


![e1v](https://github.com/fmerizzi/text_style_comparison/blob/main/text_inpainting/res_mask3.png)

