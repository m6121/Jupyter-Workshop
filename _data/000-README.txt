Project_title: KTA-Carrots
Project_id: D2011-KTA-KHY
Label: 
Study: Activity recognition of kitchen task (cooking carrots soup)
Pi-Name (creator): Frank Krüger, Albert Hein, Kristina Yordanova, Thomas Kirste
Pi-Email: {frank.krueger2,albert.hein,kristina.yordanova,thomas.kirste}@uni-rostock.de
Pi-Affiliation: MMIS
Date <create date>: 2011
Type: measurement
Location (place): SmartLab 321, Albert-Einstein-Straße 22
Keywords: activity recognition, kitchen task assessment

Objective (Goal):
Recognise the actions of a user while executing kitchen tasks.

Problem-Statement:
One person is preparing a meal in the kitchen that includes:
- preparing the ingredients for a soup
- cooking the soup
- serving the soup 
- having meal
- cleaning the table
- washing the dishes
The task is to recognise the fine-grained actions that constitute these tasks and the objects in the environment.

Description:
This Dataset was recorded during the diplom thesis of Fabian Wolff.
The results from the dataset can be found in "Computational State Space Models for Activity and Intention Recognition. A Feasibility Study" by Krüger et al.
It contains 7 datasets that describe the execution of preparing and having a meal.
The sensor data was recorded with motion capturing system based on wearable inertial measurement units (IMUs).
For each sensor three axis acceleration and angular rates were recorded, with a sampling rate of 120 Hz.
Each dataset contains of the raw IMU data and the corresponding annotation.
The annotations are described in the form 'action-object-fromLocation-toLocation'.

16 action classes were annotated:
- wash
- wait
- move
- take
- put
- cut
- fill
- turn_on
- cook
- turn_off
- open
- close
- sit_down
- eat
- drink
- stand_up

4 locations were annotated:
- sink
- moving
- counter
- table

6 fixed places were annotated:
- sink
- moving
- counter
- table
- stove
- cupboard

11 objects were annotated:
- hands
- carrot
- knife
- cutting_board
- pot
- wooden_spoon
- plate
- glass
- bot- tle
- spoon
- sponge


