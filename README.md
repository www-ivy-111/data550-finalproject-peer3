# About the dataset
You could skip this part if not interested in the science backgroud)

This is a spatial transcriptomics dataset.  
The dataset comprises spatial transcriptomics information within a mouse brain and is stored as a Seurat object. It includes counts information, representing RNA counts or gene expression in each spot, as well as coordinate information, indicating the physical coordinates of each spot.
Exploring the dataset enables us to grasp the spatial intricacies within the mouse brain, identifying key genes prevalent in each distinct brain region, and subsequently establishing connections between gene expression patterns and brain functionality.

*Note*:

Please be patient while working with the dataset; the data is high-dimensional and processing may be slow.

You have several ways to read in the dataset.  
1. Using the 10X function to read in the dataset (recommend).  
2. Download the dataset from [https://www.10xgenomics.com/datasets/mouse-brain-serial-section-2-sagittal-posterior-1-standard-1-0-0](10X website) and read in the local dataset. At least "Feature/barcode matrix HDF5 (filtered)" and "Spatial imaging data" should be downloaded.

# How to run the program
If this is your first time working with RNA data, the initial setup may take a few minutes as you install necessary packages.

All code files are located in the 'code' folder. Using 'make' simplifies the process of running all codes and generating the report file. However, if you're unfamiliar with 'make', you can run the files individually starting with '00_read_data.Rmd', followed by '01_make_table1.R', '02_make_plots.R', and finally '03_render_report.R'.

Tables and plots will be generated in the 'output' folder, while the final report will be found in the main folder.

Traditionally, tables are not the preferred method for visualizing gene data. Nonetheless, in adherence to assignment requirements, we will include tables to represent the gene data.


# Code Description

`code/00_read_data.R`
- read raw data from online or `raw_data/` folder
- save clean data in `derived_data/` folder

`code/01_make_table1.R`
- read clean data from `derived_data/` folder
- save table 1 in `output/tables/` folder

`code/02_make_plots.R`
- read clean data from `derived_data/` folder
- save scatter plot in `output/figures/` folder

`code/03_render_report.R`
- render `report.Rmd` 
- save compiled report in main folder

`code/report.Rmd`
- read data, tables, and figures from respective locations
- display results for production report