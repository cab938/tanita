# Tanita Data Format
The tanita measurement datafiles can be found in the `TANITA\GRAPHV1\DATA` directory with the name of `DATA1.CSV`...`DATA4.CSV` where each file corresponds to a slot (button) on the scale. Individual profile data can be found for users in `TANITA\GRAPHV1\SYSTEM` directory with the name of `PROF1.CSV`...`PROF4.CSV`.

Each measurement file is comma separated, where a given line indicates a measurement for a user in that slot. Instead of headers for the csv, each row has header information embeded in it, where column `i` is the header for the data field in column `i+1`. Each even column (0, 2, 3 ...) is a header, and headers are always two characters in length. The mappings for the Tanita BC-603 FS scale are below (note: this scale seems to be the same as the BC-601, and the datafiles even incorrectly note the model number as the BC-601).

```
"{0": "Unknown: 16"
"~0": "Length unit (metric = 2) "
"~1": "Mass unit (metric = 2)" 
"~2": "Unknown"
"~3": "Unknown"
"Bt": "Body type (athlete or not, male athlete = 2, male non-athlete = 0)"
"Wk": "Weight"
"MI": "Body mass index (BMI)"
"MO": Model
"DT": Measurement Date
"Ti": Measurement Time
"GE": Gender (male = 1)
"AG": Age
"Hm": Height
"AL": "Activity Level (1-3 according to set value. Athlete is always 3 and shifts data like basal and muscles even slightly above non-athlete with level 3 activity)"
"FW": "Global fat %"
"Fr": "Arm fat (right) %"
"Fl": "Arm fat (left) %"
"FR": "Leg fat (right) %"
"FL": "Leg fat (left) %"
"FT": Torso fat %"
"mW": "Global muscle (kg)"
"mr": "Arm muscle (right) (kg)"
"ml": "Arm muscle (left) (kg)"
"mR": "Leg muscle (right) (kg)"
"mL": "Leg muscle (left) (kg)"
"mT": "Torso muscle (kg)"
"bw": "Estimated bone mass (kg)"
"IF": "Visceral fat rating"
"rA": "Estimated metabolic age"
"rD": "Daily calorie intake (DCI). Not basal! Basal may be calculated using coefficients linked to the activity level and gender. See below"
"ww": "Global body water %"
"CS": "Unknown: BC, this does change per entry"


Daily Calorie Intake = BMR * Activity level coefficient
Female activity level 1 coeff = 1.56
Female activity level 2 coeff = 1.64
Female activity level 3 coeff = 1.82
Male activity level 1 coeff = 1.55
Male activity level 2 coeff = 1.78
Male activity level 3 coeff = 2.10
```
