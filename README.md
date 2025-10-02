# README.md

## ucrt64 bash   
  
```rm -rf build/ucrt64-gcc```   
```cmake --preset ucrt64-gcc```   
```cmake --build --preset ucrt64-gcc```   


## install clarification
vs code taskbar configuration only does configurations and build, NOT intall.  
Install must be initiated via terminal, bash (gcc) or developer powershell (MSVC).  
Outputs just outputs but install installs, in order to maintain separtion  

### gcc install, ucrt64 bash
```cmake --install build/ucrt64-gcc```  
### MVSC intall, PowerShell     
```cmake --install build/release --config Release```  

