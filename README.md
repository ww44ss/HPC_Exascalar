# HPC_Exascalar

This repository contains data on the Top500 Supercomputers from 2011 to present.. The data are from the [Top500](top500.org) and [Green500](green500.org) websites. 

The raw data from each website are saved as lightly cleaned .csv files in respective directories. Some cleaning was necessary, especially on the Green500 lists, to ensure data completeness (for example one instance didn't contain the corresponding Top500 ranking, which was used to concatenate the lists) and consitency (an early version of the Green500, for instance, gave ~equivalent Green systems the same ranking, a practice later dropped).

All the data are combined, using `Exascalar_Cleaner.R` into a single large data file (containing ~9500 rows and 39 columns) with cleaned variable names, which is save here. Since the earliest list used has about 25 observations per computer and the current lists tracks almost 40 variables, many data are incomplete. 

Exascalar.csv
 [1] "rank": Performance Ranking by performance
 [2] "previousrank": Rank on the previous list             
 [3] "firstappearance": The list on which the system first appeared (this is encoded by number, and needs to be translated to a date.
 [4] "firstrank": Rank when it first appeared                  
 [5] "name": Short supercomputer name
 [6] "computer": longer description of the computer                   
 [7] "site": lab name, etc.
 [8] "manufacturer": who made it             
 [9] "country": 
 [10] "year": year it was made        
[11] "segment":                      "totalcores"                 
[13] "acceleratorcoprocessorcores" "rmax"                       
[15] "rpeak"                       "nmax"                       
[17] "nhalf"                       "power"                      
[19] "powersource"                 "mflopsperwatt"              
[21] "architecture"                "processor"                  
[23] "processortechnology"         "processorspeed.mhz"         
[25] "operatingsystem"             "osfamily"                   
[27] "acceleratorcoprocessor"      "corespersocket"             
[29] "processorgeneration"         "systemmodel"                
[31] "systemfamily"                "interconnectfamily"         
[33] "interconnect"                "region"                     
[35] "continent"                   "date"                       
[37] "green500rank"                "green500power"              
[39] "Exascalar" 






