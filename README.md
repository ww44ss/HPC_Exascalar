# HPC_Exascalar

This repository contains data on the Top500 Supercomputers from November 2011 to present. The data are copied from the [Top500](top500.org) and [Green500](green500.org) websites, and presented in combined form as a single file `BigExascalar.csv`, with each system (500 per list) assigned a corresponding list.date and associated variables from the two lists.  

### Data Methods:
The raw data from each website are saved as lightly cleaned .csv files in respective directories. Some cleaning was necessary, especially on the Green500 lists, to ensure data completeness (for example one instance didn't contain the corresponding Top500 ranking, which was used to concatenate the lists) and consitency (an early version of the Green500, for instance, gave ~equivalent Green systems the same ranking, a practice later dropped).

All the data are combined, using `Exascalar_Cleaner2.R` into a single large data file (containing ~9500 rows and 39 columns in November 2016) with cleaned variable names. As the earliest list (2007) had about 25 observations per computer and the current lists tracks almost 40 variables, many data are incomplete over the entire time-span. 

### Variables in `Exascalar.csv`:  
 - __rank:__ System Ranking by performance (e.g. 1) for given date.  
 - __previousrank:__ System rank on the previous list (e.g. _NA_).             
 - __firstappearance:__ The list on which the system first appeared (needs to be translated.) (e.g. 41)
 - __firstrank:__ Rank when system first appeared on a list (e.g. 1)                 
 - __name:__ Short system name (e.g. ("Sunway TaihuLight")
 - __computer:__ longer description of the computer(e.g. "BlueGene/Q, Power BQC 16C 1.60 GHz, Custom")                   
 - __site:__ generally a lab or university name, etc. (e.g. "DOE/SC/LBNL/NERSC")
 - __manufacturer:__ who made the system. (e.g. "Cray")            
 - __country:__ where the system is loacted (e.g. "China")
 - __year:__ year system was made (e.g. 2012)       
 - __segment:__ economic segment (e.g. "Research")  
 - __totalcores:__ total cores in system (e.g. 1572864 )                   
 - __acceleratorcoprocessorcores:__ number of co-processor cores (e.g. 230000).    
 - __rmax:__ max performance (used for Top500 ranking).                        
 - __rpeak:__ peak instantaneous peroformance. 
 - __nmax:__ max of n                   
 - __nhalf:__ half of n
 - __power:__ power as reported in Top500 list.                       
 - __powersource:__ was the data submitted or inferred.  
 - __mflopsperwatt:__ efficiency in megaflops per watt.              
 - __architecture:__ description of system architecture.  
 - __processor:__ long processor descriptions (e.g. "Intel Xeon E5-2692v2 12C 2.2GHz").                  
 - __processortechnology:__ short description (e.g. "Intel IvyBridge").
 - __processorspeed.mhz:__ clock speed in mhz (e.g. 1450).        
 - __operatingsystem:__ operating system detailed descrition (e.g. "Cray Linux Environment").  
 - __osfamily:__ short description (e.g. "Linux").                    
 - __acceleratorcoprocessor:__ long description of accelerator co-processor (e.g. "NVIDIA Tesla K20x").  
 - __corespersocket:__ a number (e.g. 260).              
 - __processorgeneration:__ processor description (e.g. "Opteron 6200 Series \"Interlagos\"").  
 - __systemmodel:__ Model name from manufacturer (e.g. "Cray XK7").                
 - __systemfamily:__ Family name of system (e.g. "Cray XK").  
 - __interconnectfamily:__ high level interconnect description (e.g. "Custom Interconnect").          
 - __interconnect:__ description of interconnect (e.g. "Cray Gemini interconnect").  
 - __region:__ where it is (e.g. "Eastern Asia").                    
 - __continent:__ where it is (e.g. "Asia").  
 - __list.date:__ listdate by year-month (day is always -01) (e.g. "2016-11-01" or "2016-06-01").                        
 - __green500rank:__ green 500 rank for specific data (e.g. 135).  
 - __green500power:__ power in kWatt as reported by green500 list.(e.g. 17808).              
 - __Exascalar:__ computed exascalar Exascalar = (log10(rmax\*10^3/ExaPerf) + log10(mflopsperwatt/(ExaEff)))/sqrt(2)) 

### note:  
The raw versions of the Top500 data (as .xls files) are stored in the /Top500data/Top500raw directory. Since the Green500 were (until November 2016) avaiable online at .csv files, these are stored as lightly cleaned files in the /Green500 directory. 






