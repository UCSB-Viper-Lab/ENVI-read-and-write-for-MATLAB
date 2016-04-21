# ENVI-read-and-write-for-MATLAB
these are codes for the functions to read and write ENVI files to MATLAB

# example
this is an exsample of how you would implement these functions in your own script

data_code='F:\Sensitivity_Analysis_20141212\Code\X_Analyze_Results\';
% Directory for data inputs (use trailing backslash)
data_folder='F:\Sensitivity_Analysis_20141212\Data_Analyze_Results\sensitivity_analysis\';

% This is name of the file.
file_synthetic='sensitivity_analysis_4_alb50_ch4_25_102_by_100_attrib'
header_synthetic='sensitivity_analysis_4_alb50_ch4_25_102_by_100_attrib.hdr';

%Read synthetic radiance and header info
cd(data_code);
data_synthetic=enviread(strcat(data_folder,file_synthetic));
info_synthetic=read_envihdr(strcat(data_folder,header_synthetic));

% the image is now an array that lookes something like this... data_synthetic(sample, line, Band)
