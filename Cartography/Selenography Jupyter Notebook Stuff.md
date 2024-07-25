# Selenography Jupyter Notebook Stuff

## Jupyter Notebook on Sagemaker Notebook

(Note: there is an IAM role on the S3 permissions that allows Jupyter notebook to do this)

[[Selenography/Cartography/Selenography Jupyter Notebook Stuff/AmazonSageMakerFullAccess]]

[[Selenography/Cartography/Selenography Jupyter Notebook Stuff/AmazonSageMaker-ExecutionPolicy]]

import pandas as pd

bucket='s3-windows-test'

data_key = 'Selenography POI CSV.csv'

data_location = 's3://{}/{}'.format(bucket, data_key)

df = pd.read_csv(data_location)

df.head()

df["Type"].count()

TypeCount = df.groupby("Type").size()

print(TypeCount)

import matplotlib.pyplot as plt

plt.clf()

TypeCount.plot(kind="bar")

plt.ylim(0,200)

plt.show()

import matplotlib.pyplot as plt

plt.clf()

TypeCount.plot(kind="bar")

plt.show()

CraterDF = df[df.Type == "Crater, craters"]

CraterDF.head()

CraterDF.Diameter.plot(kind='hist', bins = 10)

plt.title('Distribution of Craters Based on Size')

plt.xlabel('Diameter of Craters')

plt.ylabel('Number of Craters')

plt.xticks([0, 50, 100, 150, 200, 250, 300, 350, 400, 450, 500],[0, 50, 100, 150, 200, 250, 300, 350, 400, 450, 500] )

plt.show()

CraterDF.Center_Lat.plot(kind='hist', bins = 2, facecolor = 'g')

plt.title('Distribution of Craters in Northern and Southern Hemispheres')

plt.xlabel('Hemisphere Location: Southern = -90 to 0; Northern = 0 to 90')

plt.ylabel('Number of Craters')

plt.xticks([-180:-1, 0:180],['Northern', 'Southern'])

plt.show()

CraterDF.Center_Lon.plot(kind='hist', bins = 2, facecolor = 'r')

plt.title('Distribution of Craters in Western and Eastern Hemispheres')

plt.xlabel('Hemisphere Location: Western = -90 to 0; Eastern = 0 to 90')

plt.ylabel('Number of Craters')

plt.show()

MareDF = df[df.Type == "Mare, maria"]

MareDF.head()

MareDF.Diameter.plot(kind='hist', bins = 4)

plt.title('Distribution of Mare Based on Size')

