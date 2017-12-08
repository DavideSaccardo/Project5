# Project5

In these folders, it can be found the code to study the 1-2D diffusion equation and the code to consider a gelocial case of the heat equation. In particular:
\begin{enumerate}
\item[-] Matlab: it contains the script used to mak al the plot shown in the paper;
\item[-] Codes:
	\begin{enumerate}
	\item[*] Diffusion equation: $\mathrm{main.cpp}$ contains the main program to choose all the boundary conditions, spatial and temporal step size and the loop to get the solution at a a give time. 

$\mathrm{pde_diffusion.cpp}$ and $\mathrm{pde_diffusion.h}$ is a class which constains all the main method to solve the diffusion equation in 1D and 2D. $\mathrm{

data_analysis.cpp}$ and $\mathrm{data_analysis.h}$ is a class used to write to file and print to screen information.
To compile: c++ -o run.x *.cpp.

	\item[*] Geological case: it contains the code (geological_1d.cpp) for the gological case. It's written to have the Number of points ($N$) for the spatial dimension ($\mathrm{time_resol}$) and the time resolution constant. Indeed if you want to change them you have to re-declare them at the beginning. However, the choice set is good: we have a good speed and good results. Furthermore if one changed N, he/she would have had to change a bit the function heat: in fact this function is written purposely with the configuration chosen, if you change N, the function probably won't take appropriately the limits 20-40-120 kilometers. The values of $\mathrm{initial_time}, \mathrm{initial_y},\mathrm{final_time},\mathrm{final_y} are set accordingly with the case considered. Note: you can set $\mathrm{flag}=0$ if you want to consider the case without radioactive decay, which is just useful in our case to reach a steady state; set $\mathrm{flag}=1$ if you want to consider the case with radioactive decay with as initial considition the steady state of the case before. 
To compile: c++ -o run.x geological_1d.cpp.

	\end{enumerate}
\end{enumerate}

Note: there aren't examples of data because they are to heavy (380 MB, for the geological case).
