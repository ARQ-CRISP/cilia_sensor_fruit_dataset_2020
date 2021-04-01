# Cilia sensor - fruit testing dataset 

Author: Pedro Ribeiro
Contact: pribeiro@inesc-mn.pt

Affiliations: 
- INESC - Microsystems and Nanotechnologies, Lisbon, Portugal
- CRISP, ARQ, Queen Mary University of London, London, United Kingdom
- Instituto Superior Técnico, University of Lisbon, Lisbon, Portugal

The files in this compressed folder comprise a dataset obtained from testing fruits at different stages of ripeness, using a tactile sensor inspired on the ciliary tactile structure found in insects.
This is (a large) part of the data used for the methods and results obtained in the work "[Fruit quality control by surface analysis using a bio-inspired soft tactile sensor][paperdoi]" presented at IROS 2020. In this work, you can also find a description of the sensor and used experimental method.

Within this dataset, you can find three folders:

- **9cilia_1_6_mm**: Data obtained for a cilia sensor with a 3x3 matrix of cilia with 1.6 mm height and 360 um diameter
- **9cilia_3_mm**: Data obtained for a cilia sensor with a 3x3 matrix of cilia with 3 mm height and 400 um diameter
- **single_3_mm**: Data obtained for a cilia sensor with a single cilium with 3 mm height and 400 um diameter

Within each of these folders, you can find a folder for each of the tested fruits (Braeburn apples or Sabrina strawberries), and within the fruit folder you may find the data for the sensor and each of the tested fruits. 
The filename structure is **(old/ripe)XX_tY**.txt:

- **old/ripe** indicates whether the data refers to a ripe or an old (rotten) fruit
- **XX** which is the tested fruit (fruit #XX)
- **Y** indicates which area of the fruit was tested (each fruit was tested in two different areas)

Each data file is comprised of 6 data rows:

- **Timestamp**: The instant in time when the datapoint was read from the sensor
- **Action**: Not relevant for this dataset
- **X, Y and Z**: Position of the sensor in space (the sensor moves in the X direction during the experiment and therefore Y and Z are approximately contant in this dataset)
- **Sensor 1**: Datapoint measured from the sensor

As described in the paper mentioned above, the data consists of 15 scans of a certain fruit region. The first 5 scans were made for adjustment of the cilia position and therefore I recommend using only the last 10 scans and discarding the first 5.
Furthermore, to separate the scans, I recommend using the **X** data as a separation criterion, as there will be a large jump in this coordinate between the end of a previous measurement and a new one (e.g. the X value at the end of a scan in 3.7 and at the beginning is -0.4 - a different scan starts when X jumps from 3.7 -> -0.4 in two consecutive lines of data).

   [paperdoi]: <https://doi.org/10.1109/IROS45743.2020.9340955>
