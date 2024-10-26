# Etna_and_Streamlit
Working with Time Series [(Etna framework)](https://github.com/etna-team/etna) and creating GUI via streamlit

# Instruction how to build the standalone app

1. Create ```*.py``` file which you want to pack into the executable installer.

2. Install the Pyinstaller library (use the ```pip install pyinstaller``` command).

3. If your file can be run without using the command line, then write the command 
```pyinstaller /path/to/yourscript.py```.

4. If you need a console to run your code, create a new file in which you pass the command to run 
and repeat the 3rd step.
  
      Here is a code example:
```bash
import subprocess
process = subprocess.Popen(['cmd'], stdin=subprocess.PIPE, stdout=subprocess.PIPE)
process.stdin.write('streamlit run yourscript.py\n'.encode())
out, err = process.communicate()
print(out.decode())
```
> [!WARNING]
IMPORTANT NOTE:  
  If you are creating a start file, your '.exe' file and the script must be in the same directory.
