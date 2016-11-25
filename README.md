# HPC_Exascalar

This repository contains data on the Top500 Supercomputers from 2011 to present.. The data are from the [Top500](top500.org) and [Green500](green500.org) websites. 

The raw data from each website are saved as lightly cleaned .csv files in respective directories. Some cleaning was necessary, especially on the Green500 lists, to ensure data completeness (for example one instance didn't contain the corresponding Top500 ranking, which was used to concatenate the lists) and consitency (an early version of the Green500, for instance, gave ~equivalent Green systems the same ranking, a practice later dropped).

All the data are combined, using `Exascalar_Cleaner.R` into a single large data file (containing ~9500 rows and 39 columns) with cleaned variable names, which is save here. Since the earliest list (2007) has about 25 observations per computer and the current lists tracks almost 40 variables, many data are incomplete over the entire timespan. 

Exascalar.csv  
 [1] "rank": System Ranking by performance (e.g. 1) for given date.  
 [2] "previousrank": System rank on the previous list (e.g. NA).             
 [3] "firstappearance": The list on which the system first appeared (encoded by number, needs to be translated.) (e.g. 41)
 [4] "firstrank": Rank when system first appeared on a list (e.g. 1)                 
 [5] "name": Short system name (e.g. ("Sunway TaihuLight")
 [6] "computer": longer description of the computer(e.g. "BlueGene/Q, Power BQC 16C 1.60 GHz, Custom")                   
 [7] "site": generally a lab or university name, etc. (e.g. "DOE/SC/LBNL/NERSC")
 [8] "manufacturer": who made the system. (e.g. "Cray")            
 [9] "country": where the system is loacted (e.g. "China")
 [10] "year": year system was made (e.g. 2012)       
[11] "segment": economic segment (e.g. "Research")  
[10] "totalcores": total cores in system (e.g. 1572864 )                   
[13] "acceleratorcoprocessorcores": added in about 2012, tracking emergence of accelerators. 
[14] "rmax": max performance (used for Top500 ranking).                       
[15] "rpeak": peak instantaneous peroformance. 
[16] "nmax":                     
[17] "nhalf":
[18] "power": power as reported in Top500 list.                       
[19] "powersource": was the data submitted or inferred.  
[20] "mflopsperwatt": efficiency in megaflops per watt.              
[21] "architecture": description of system architecture.  
[22] "processor": long processor descriptions (e.g. "Intel Xeon E5-2692v2 12C 2.2GHz")                
[23] "processortechnology": short description (e.g. "Intel IvyBridge").
[24] "processorspeed.mhz": clock speed in mhz (e.g. 1450).        
[25] "operatingsystem": operating system detailed descrition (e.g. "Cray Linux Environment").  
[26] "osfamily": short description (e.g. "Linux").                    
[27] "acceleratorcoprocessor": long description of accelerator co-processor (e.g. "NVIDIA Tesla K20x")
[28] "corespersocket": a number (e.g. 260)            
[29] "processorgeneration": processor description (e.g. "Opteron 6200 Series \"Interlagos\"")
[30] "systemmodel": Model name from manufacturer (e.g. "Cray XK7")               
[31] "systemfamily": Family name of system (e.g. "Cray XK")
[30] "interconnectfamily": high level interconnect description (e.g. "Custom Interconnect")         
[33] "interconnect": description of interconnect (e.g. "Cray Gemini interconnect")
[34] "region": where it is (e.g. "Eastern Asia")                    
[35] "continent": where it is (e.g. "Asia")
[36] "date": data of list - this is added by me (e.g. "2016-11-01" or "2016-06-01")                       
[37] "green500rank": green 500 rank for specific data (e.g. 135)
[38] "green500power": power in kWatt as reported by green500 list.(e.g. 17808)              
[39] "Exascalar":computed exascalar Exascalar = (log10(rmax\*10^3/ExaPerf) + log10(mflopsperwatt/(ExaEff)))/sqrt(2)) 






