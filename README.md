# Azimuth-Data-Analysis-Task

This repository contains the analysis and clustering of data about the PoFC cells found in human brain and predict the cell types for each file. This task was performed analysis on the cells and filtered these cells using QC metrics.

## The Steps we performed for this task are:
1) Download the files using the following filters from www.portal.nemoarchive.org

![Capture](https://user-images.githubusercontent.com/17748119/164366725-3a1d2116-b54a-4b45-808c-db3d75da1538.PNG)

2) Now the files along with their urls are saved in a manifests file which is downloaded.

![image](https://user-images.githubusercontent.com/17748119/164367197-945220dc-7756-4cee-93df-d7b2efaf17f4.png)

3) Now to download all these files from the manifests file we use a client called portal_client. This portal_client is a python-based client for downloading data files hosted by the an instance of the portal software developed by the GDC and further modified by the Institute for Genome Sciences (IGS).
Type the commands given below:

```
git clone https://github.com/IGS/portal_client
```

![resized-image-Promo](https://user-images.githubusercontent.com/17748119/164380871-e8503019-32ca-43a4-bd14-7107809dacae.jpeg)
 
  ```
python3 -m venv --copies VENV_portal_client
```

 ```
source VENV_portal_client/bin/activate
```

 ![WhatsApp Image 2022-04-21 at 12 08 58 AM](https://user-images.githubusercontent.com/17748119/164371929-1ec84c70-ce2e-4924-9679-60860caa16b8.jpeg)

 ```
pip install -r portal_client/requirements.txt
```

 ![WhatsApp Image 2022-04-21 at 12 10 26 AM](https://user-images.githubusercontent.com/17748119/164372020-e1eb53f4-49fa-4d92-813e-cbd2feba7ed4.jpeg)
 
 ```
cd portal_client
```

 ```
easy_install . 
```

 ![WhatsApp Image 2022-04-21 at 12 12 04 AM](https://user-images.githubusercontent.com/17748119/164372062-b77a88a5-a6a9-45c6-85ed-92bd807fdf0c.jpeg)

 
4) This client takes the downloaded .tsv file or the manifest file as an input and extracts and downloads the files from the given urls in the file. All files are automatically downloaded using this client

 ```
portal_client --manifest /path/to/reference_file.tsv 
```

 ![WhatsApp Image 2022-04-21 at 12 19 30 AM](https://user-images.githubusercontent.com/17748119/164372090-2f9e7f17-f67b-47f7-a2b2-7094be96519b.jpeg)


5) For this task, we need to have R. If you do not have it, you can follow this [tutorial](https://www.datacamp.com/community/tutorials/installing-R-windows-mac-ubuntu) 


6) Find the R installation and add the path to your environment to access R from the command line ([Reference](https://helpdeskgeek.com/windows-10/add-windows-path-environment-variable/)

