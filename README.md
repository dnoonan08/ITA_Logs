Data logs from December 2021 run of ECON-T at ITA.

 - I2C_Logs: outputs of I2C checks during spills, very messy timestamps from hexacontroller (output of https://github.com/cmantill/econt_sw/blob/master/econt_sw/ITA_Testing.py)
 - I2C_Logs_FixedDates: copy of I2C_Logs, but after being run through FixLogDates.ipynb, which corrects the timestamps as best as possible
 - Currents: outputs of current monitoring scripts (https://github.com/dnoonan08/ITA_Scripts/blob/main/CurrentMonitoring.py)
 - protonCount.csv: beam monitoring data (from https://github.com/dnoonan08/ITA_Scripts/blob/main/integrateITA_ExtrapoPlot.py)

Scripts/Notebooks:
 - BeamCalc.ipynb reads in protonCount.csv, and calculates proton flux on ECON based on motion table positions, produces fullProtonInfo.csv which contains these extra columns
 - FixLogDates.ipynb attempts to rectify differences in dates from hexacontroller log files and real time (matching timestamps from log files to timestamps of when beam arrived or from notes taken during testings)
 - LogParsing.ipynb parses the log files in I2C_Logs_FixedDates to find and graph errors