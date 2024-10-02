# gpuAugLISI

We have developed a GPU-accelerated augLISI. The CPU version of augLISI is displayed on [augLISI](https://github.com/egbdfX/Intensity-sensitive-IQAs?tab=readme-ov-file#auglisi-auglisipy). Please see our paper in Section [Reference](https://github.com/egbdfX/gpuAugLISI/tree/main#reference) for more information.

## User guidance

**Step 1:**
Make sure GCCcore, CUDA, and CFITSIO are avaiable. If you see a warning saying ```/usr/bin/ld.gold: warning: /apps/system/easybuild/software/GCCcore/11.2.0/lib/gcc/x86_64-pc-linux-gnu/11.2.0/crtbegin.o: unknown program property type 0xc0010002 in .note.gnu.property section```, you would need to make sure Python is also available.

**Step 2:**
Run the Makefile by ```make```. Note that this Makefile is written for NVIDIA H100. If you are using other GPU, you would need to make sure the CUDA arch is matching.

**Step 3:**
Run the code by ```./sharedlibrary_gpu x.fits y.fits```, where ```x.fits``` and ```y.fits``` are the two input images (FITS files). The two input images should have the same size.

**Step 4:**
The code will output a FITS file named ```output_augLISI.fits```, which is the output augLISI matrix.

## Contact
If you have any questions or need further assistance, please feel free to contact at [egbdfmusic1@gmail.com](mailto:egbdfmusic1@gmail.com).

## Reference

**When referencing this code, please cite our related paper:**

X. Li, K. Adámek, and W. Armour, "Intensity-Sensitive Quality Assessment of Extended Sources in Astronomical Images," The Astrophysical Journal Supplement (ApJS) Series, vol. 274, no. 2, 2024, pp. 37, doi: 10.3847/1538-4365/ad6a58.

X. Li, K. Adamek, and W. Armour, "GPU Accelerated Image Quality Assessment-Based Software for Source Detection," Astronomical Data Analysis Software and Systems (ADASS) XXXIV, 2024. 

## License

Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
