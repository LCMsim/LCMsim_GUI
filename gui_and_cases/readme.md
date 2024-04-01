Use folder gui_and_cases. 
The intended operating system for LCMsim v2 GUI is Windows. The software was extensively tested for Windows 10. In order to use LCMsim for filling simulations perform the following steps:
- Download Julia from https://julialang.org/downloads/
- Install Julia and add an environment variable such that the Julia terminal can be started from the command line.
- Open a Julia terminal.
- For LCMsim v2: Change to package manager with "]" and "add HDF5 CSV JLD2 ProgressMeter GeometryBasics LinearAlgebra StaticArraysCore Printf" and return with the backspace key
- For the GUI: Change to package manager with "]" and "add Gtk GLMakie Makie NativeFileDialog GeometryBasics HDF5" and return with the backspace key
- Close the Julia terminal.
- Create a repository folder in the file explorer for the solver, e.g. D:\programs\LCMsim_v2\solver
- Download the LCMsim v2 repository from https://github.com/LCMsim/LCMsim_v2.jl. LMB on the green Code button and select Download ZIP. Extract the content in the repository folder.
- Create a repository folder in the file explorer for the gui and the cases, e.g. D:\programs\LCMsim_v2\gui
- Download the LCMsim gui repository from https://github.com/LCMsim/LCMsim_GUI. LMB on the green Code button and select Download ZIP. Extract the content in the repository folder.
- Optionally, copy the cases folder to a different location
- Change to the cases folder
- Configure the settings in lcmsim_config.jl: 
i_batch=0 (parameter input in GUI), =1 (read from text files), 
i_model=1 (RTMsim), =2 (LCMsim), =3 (VARIsim, not yet implemented in GUI), 
i_mesh=1 (NASTRAN with sets), =2 (ABAQUS with sets), 
repositorypath= path to folder with the solver repository is located, with "\\" as separator instead of "\"
guipath= path to folder where the gui jl-file is located
- In the cases directory, double click on lcmsim_launch.bat to start the GUI.
