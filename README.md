# Tanita Data Format
The tanita measurement datafiles can be found in the `TANITA\GRAPHV1\DATA` directory with the name of `DATA1.CSV`...`DATA4.CSV` where each file corresponds to a slot (button) on the scale. Individual profile data can be found for users in `TANITA\GRAPHV1\SYSTEM` directory with the name of `PROF1.CSV`...`PROF4.CSV`.

Each measurement file is comma separated, where a given line indicates a measurement for a user in that slot. Instead of headers for the csv, each row has header information embeded in it, where column `i` is the header for the data field in column `i+1`. Each even column (0, 2, 3 ...) is a header, and headers are always two characters in length. The mappings for the Tanita BC-603 FS scale are below (note: this scale seems to be the same as the BC-601, and the datafiles even incorrectly note the model number as the BC-601).

```
"{0": "Unknown: 16"
"~0": "Length unit"
"~1": "Mass unit"
"~2": "Unknown: 4"
"~3": "Unknown: 3"
"Bt": "Unknown: 2, it has something to do with the athlete mode. When I set male athelete it is 2, when I set male it is 0"
"Wk": "Body mass"
"MI": "Body mass index (BMI)"
"MO": Model
"DT": Measurement Date
"Ti": Measurement Time
"GE": Gender
"AG": Age
"Hm": Height
"AL": Activity Level
"FW": "Global fat %"
"Fr": "Arm fat (right) %"
"Fl": "Arm fat (left) %"
"FR": "Leg fat (right) %"
"FL": "Leg fat (left) %"
"FT": Torso fat %"
"mW" = "Global muscle %"
"mr" = "Arm muscle (right) %"
"ml" = "Arm muscle (left) %"
"mR" = "Leg muscle (right)%"
"mL" = "Leg muscle (left) %"
"mT" = "Torso muscle %"
"bw": "Estimated bone mass"
"IF": "Visceral fat rating"
"rA": "Estimated metabolic age"
"rD": "Daily calorie intake (DCI)"
"ww": "Global body water %"
"CS": "Unknown: BC, this does change per entry"
```
