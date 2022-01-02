![GMIT Logo](data\gmitlogo.jpg)

# Fundamentals of Data Analysis Project
The purpose of this repository is for project submission for the Fundamentals of Data Analysis assessment in Galway-Mayo Institute of Technology for the academic year 2021/2022. 

<br>

***

<br>

## Project Description
The repository contains two Jupyter notebooks: 
1. cao.ipynb
2. pyplot.ipynb

<br>

***

<br>

### pyplot
The pyplot workbook provides an introduction to Matplotlib package and an overview of the pyplot sub-package.  Stateful and stateless methods of plotting are discussed and the main structures of a plot are explained such as figures, axes, axis, titles, parameters and styles.  

The workbook then provides an explanation of three plots listed below. 

- Histograms
- Scatter plots
- Box plots

The plots are then demonstrated by using [Iris Fisher dataset](https://archive.ics.uci.edu/ml/datasets/iris), and a human body mass index data set that was generated randomly using the [Numpy Random package](https://numpy.org/doc/stable/reference/random/generator.html).

<br>

***

<br>

### CAO

The CAO workbook provides a demonstration on how to load CAO points from the [CAO website](https://www.cao.ie/) for the years 2021, 2020, and 2019.  Each year held the points in a different format.  The demonstration shows how to data from a html webpage, data from a excel file and data from a PDF file. 

Each years data is loaded into an individuals Pandas dataframe before being joined to a common dataframe. 

Upon cleansing the dataframe, the points for each are compared.   The years are compared with histograms, KDE plots, bar plots and pie plots.  It was identified that the points in 2021 rose compared to those in 2020 and 2019 - particularly the courses requiring 500 - 625 points rose dramatically. 

<br>

***

<br>

## Steps to install

1. It is recommended that Windows users download Cmder to interact with the command line. Cmder can be downloaded [here](https://cmder.net/).   Mac and Linux user may continue to use the built in command line. 

2. To run this code a user will require Python 3 (available [here](https://www.python.org/downloads/) and the packages listed in the requirements.txt file.   It is however recommended that a user downloads Anaconda as these particular packages including Python 3 are already pre-installed.  You can download Anaconda [here](https://www.anaconda.com/products/individual).  

3. Users will be required to download Git in order to pull contents from the repository into a local directory. Git is available [here](https://git-scm.com/downloads). 

4.  It is recommended to user Google Chrome or Firefox to interact with Jupyter. 

<br>

***

<br>

## Run
1. To pull the code to a local directory a user will first need to clone this repository using the SSH. Go to the desired directory in the command line and type 

```
gitclone git@github.com:RYANCOX00/Fundamentals_of_DA.git
```

<br>

2. To open the directory in Jupyter type jupyter lab in the current directory on the command line. 

```
jupyter lab
```

<br>

3. The browser should open automatically, however if it does not open go to Google Chrome or Firefox and type the below in the url bar.

```
http://localhost:8888/lab/workspaces/auto-d
```

<br>

4. To run either cao.ipynb or pyplot.ipynb notebooks 
- Open the desired file in Jupyter.
- Go to *Kernel*. 
- Click *Restart Kernel and Run All Cells*. 

<br>

***

<br>

## Explore
A user can interact with interesting code on both workbooks. 

### pyplot.ipynb

Within the notebook, the below variables were created for each feature.  They contain the measurements for that feature broken down by the species of flower. 

```python

# Indexing each measurement for each specie. 

sepal_length = [setosa.iloc[:,0], versicolor.iloc[:,0], virginica.iloc[:,0]]
sepal_width = [setosa.iloc[:,1], versicolor.iloc[:,1], virginica.iloc[:,1]]
petal_length = [setosa.iloc[:,2], versicolor.iloc[:,2], virginica.iloc[:,2]]
petal_width = [setosa.iloc[:,3], versicolor.iloc[:,3], virginica.iloc[:,3]]
```

Under input 25 and input 40, only one variable was used to demonstrate the plots.  A user can interact with these plots using the variables defined above.  Also note that axes and axis labels will also need to be amended.  See the below example of code and the plot rendered. 

<br>

#### Code for comparing Iris features
```python
# Creating the labels for the legend
label = ["Setosa", "Versicolor", "Virginica"]

# Plotting the histogram. 30 bins to show variation. Stacking the species. 
plt.hist  (petal_length, bins = 30, stacked = True, label = label)


# Applying a grid (behind the bars as set in parameters)
plt.grid()

# Plotting the legend
plt.legend()

# Displaying the plot
plt.show()
```

<br>

#### Code rendered for Petal Length


![Petal_lenght](data\Petal_Lenght_snip.png)


### cao.ipynb
During the cao analysis, the *spike* and the *upper-band* thresholds were defined in input cell 54.  These can be adjusted by a user to further discover how many of the overall courses required a particular range of courses.  The KDE code at input 59 - 62 will also be adjusted by these parameters. 

Input at 54:

```python
# Creating range variables for the Spike, low and high. 
low1=  150
high1 = 349

# Creating range variables for the Upper-Band, low and high.
low2 = 350
high2 = 625
```

<br>

***

<br>

## Credits
During the cao.ipynb workbook, the code for loading cao points for 2021, 2020, and 2019 was heavily influenced by GMIT lecture, Dr Ian McLoughlin tutorial videos for the Fundamental of Data Analysis modules. Several weekly lectures focused on loading cao points from html pages, excel spreadsheets and PDF documentation.  Code used in the cao.ipynb is directly influenced from these tutorials. 

The structure and content of this readme file has also been influenced from Dr Ian McLoughlin tutorial video published on 27th November 2021 entitled *"Sketching a README"* as part of the Fundamental of Data Analysis module. 

<br>

***

<br>

## Contact
Should any person wish to contact me in relation to the content of this workbook, they can contact me on my GMIT email address: 

[G00398251@gmit.ie](mailto:G00398251@gmit.ie)

<br>

***

<br>

## Troubleshoot
Should a user experience an error when running the code in these workbooks they should ensure they have the latest version of the packages listed in the requirements.txt file.  

To update a package a user should go to the command line on their terminal and type "*pip install --upgrade [name of package]*". For example for the matplotlib package a user would type the following into the command line:

```
pip install --upgrade matplotlib

```
During this project I experience difficultly in rendering input 69 of cao.ipynb.  

The bar_label function is a new function in matplotlib since version 3.4.1.  A user will be required to update matplotlib if the version they have on their machine pre-dates this version.  See the code for the bar_label function referred to below.

```python
# Post version 3.4.1 matplotlib has bar_label function.[28]  We can added format as percentage [29]
bar.bar_label(bar.containers[0], fmt= '%.1f%%', label_type='edge')
```
 
<br>

***

<br>

## Conclusion

During this project I strongly improved my visualisation skills with pyplot.  I have developed by research skills whereby official documentation is the first point of call.  Going forward I will implement and expand on these skills in future projects. 

During the cao.ipynb I have developed new skills in python.  I'm now aware of the different data sources available and developed a sound ability to load data from an array of sources into a dataframe. I have also developed knowledge on KDE plots which I will implement into projects going forward. 


<br>

***