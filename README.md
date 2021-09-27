# createInventorSuite
MATLAB functions designed to easily create .iv files, to be viusalized in WristVisualizer.
To use, write a continuous string in MATLAB.

Example:

ivstring = createInventorHeader();

% make a semi-transparent red sphere of radius 1mm at the origin

ivstring = [ivstring createInventorSphere([0 0 0],1,[1 0 0],0.5)];

fid = fopen('filename.iv','w'); % open the file to write

fprintf(fid,ivstring); % write the string to file

fclose(fid); %  close the file


You can then open it in WristVisualizer : https://github.com/DavidLaidlaw/WristVisualizer/tree/master 
