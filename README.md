# Azimuth-Data-Analysis-Task

In this task, we are using the data about the PoFC cells found in human brain and predict the cell types for each file. We also performed analysis on the cells and filtered these cells using QC metrics.

The Steps we performed for this task are:

1) Download the files using the following filters from www.portal.nemoarchive.org

![Capture](https://user-images.githubusercontent.com/17748119/164366725-3a1d2116-b54a-4b45-808c-db3d75da1538.PNG)



2) Now the files along with their urls are saved in a manifests file which is downloaded.

![image](https://user-images.githubusercontent.com/17748119/164367197-945220dc-7756-4cee-93df-d7b2efaf17f4.png)


3) Now to download all these files from the manifests file we use a client called portal_client. This portal_client is a python-based client for downloading data files hosted by the an instance of the portal software developed by the GDC and further modified by the Institute for Genome Sciences (IGS)

4) This client takes the downloaded .tsv file or the manifest file as an input and extracts and downloads the files from the given urls in the file. All files are automatically downloaded using this client

5) 

