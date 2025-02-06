# EXE Launcher from Browser  

This web-based tool allows users to run `.exe` files directly from their browser. The tool provides a user-friendly interface for selecting and launching executable files. It runs on a **virtual machine using a modified version of BoxedWine**, allowing it to work on any operating system with a modern web browser.  

## Features  

- **Drag and Drop Support**: Users can drag and drop `.exe` or `.zip` files containing `.exe` files.  
- **File Selection**: Alternatively, users can select files using the file input button.  
- **Executable Launch**: Once an `.exe` file is selected, users can launch it with the click of a button.  
- **Zip File Handling**: If a `.zip` file containing an `.exe` is uploaded, the tool will extract and allow the `.exe` to be launched.  
- **Cross-Platform Support**: Runs on **any OS** that supports modern web browsers, as it utilizes a virtual machine based on BoxedWine.  

## Requirements  

- **Browser**: Works on **any modern browser**, including Chrome, Firefox, Edge, and Safari.  
- **Operating System**: Can be used on **any OS**, including Windows, Linux, macOS, and even mobile devices.  

## How to Use  

1. **Open the Web Page**: Visit the page where the tool is hosted.  
2. **Select or Drag and Drop Files**:  
    - Drag and drop an `.exe` file or a `.zip` file containing an `.exe` into the designated drop area.  
    - Alternatively, click the "Browse" button to select a file manually.  
3. **Launch the Executable**:  
    - Once an `.exe` file is selected, the "Launch Executable" button will appear.  
    - Click this button to execute the file within the virtual environment.  

## How It Works  

- The tool uses **a modified version of BoxedWine**, a WebAssembly-based emulator, to run Windows executables in the browser.  
- **File Processing**:  
    - If a `.zip` file is uploaded, the contents are extracted, and the `.exe` file is identified and made available for launching.  
    - If a `.exe` file is uploaded directly, it is loaded into the virtual machine for execution.  
- The page contains modals for:  
    - **Error Handling**: Displays errors if something goes wrong during file handling or execution.  
    - **Success Notifications**: Notifies the user if the executable is launched successfully.  

## Known Issues  

- **Performance Limitations**: Since the tool runs in a virtual machine within the browser, execution speeds may be slower than running `.exe` files natively.  
- **Compatibility**: Not all Windows applications may function correctly due to limitations in BoxedWine.  
- **File Size Limits**: Some browsers may impose restrictions on the size of files that can be processed.  

## Troubleshooting  

- **No Executable Selected**: Ensure you have selected a valid `.exe` or `.zip` file containing an `.exe`.  
- **Failed to Launch Executable**: Some executables may require additional dependencies not included in the virtual machine.  
- **Performance Issues**: Running larger programs may slow down execution due to WebAssembly limitations.  

## Future Plans  

Future updates aim to:  
- **Improve performance** by optimizing the virtual machine.  
- **Enhance compatibility** with more Windows applications.  
- **Add support for persistent storage**, allowing applications to save and load files between sessions.  

## Contributing  

Feel free to fork this repository, improve it, and submit pull requests. Contributions to make it more robust or support additional use cases are welcome!  

## License  

This project is open source and available under the MIT License. See the [LICENSE](LICENSE) file for more details.  

## About XPDevs  

This tool was developed and is maintained by **XPDevs**. XPDevs is committed to building simple, accessible software solutions that empower users across all platforms.