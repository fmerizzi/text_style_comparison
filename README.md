# medieval writings style comparison and restoration  
Using gram matrices to compare calligraphy from medieval frescoes + deep image prior for text restoration. 

## style comparison 
For the che style comparison we select six images all cointaining the letters "et", three come from "Cella di Macra" and three from "Venanso".

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

We then compute dissimalarity scores within the two groups and against each other. 
The score is rounded to the the 2nd decimal value and multiplied by 100 for ease of readibility. 

**result table**


![table](https://github.com/fmerizzi/text_style_comparison/blob/main/Screenshot_20221015_185331.png)

**scores**


Venanso within group dissimilarity = 0.3866

Cella di Macra extra group dissimilarity = 0.2966

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

