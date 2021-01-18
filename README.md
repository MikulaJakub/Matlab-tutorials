# Matlab-tutorials
This repository contains some simple Matlab examples

## Read all files from the directory and plot them
```Matlab
clear
clc

files = dir('*');

for (i=3:max(size(files)))
load(files(i).name)
end 

w = who;
for (i=1:max(size(files))-2)
	value = eval(w{i});
	plot(value(:,1),value(:,2),'-')
	hold on
end
```
