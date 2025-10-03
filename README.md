## ucrt64 bash
```bash
# Clean previous build artifacts
rm -rf build/ucrt64-gcc

# Configure using ucrt64-gcc preset
cmake --preset ucrt64-gcc

# Build using the same preset
cmake --build --preset ucrt64-gcc

```
## install clarification
vs code taskbar configuration only does configurations and build, NOT intall.  
Install must be initiated via terminal, bash (gcc) or developer powershell (MSVC).  
Outputs just outputs but ins tall installs, in order to maintain separtion  

## gcc install with ucrt64 bash
```bash
# Install outputs from ucrt64-gcc build directory
cmake --install build/ucrt64-gcc
```
### MSVC intall PowerShell  
```powershell
# Install outputs from MSVC build directory
cmake --install build/release --config Release
```

