# EXE Launcher from Browser

This simple web-based tool allows users to run `.exe` files directly from the browser. The tool checks for the required environment and provides a user-friendly interface for selecting and launching executable files. It works specifically in Internet Explorer (IE) due to its reliance on ActiveX technology.

## Features

- **Drag and Drop Support**: Users can drag and drop `.exe` or `.zip` files containing `.exe` files.
- **File Selection**: Alternatively, users can select files using the file input button.
- **Executable Launch**: Once an `.exe` file is selected, users can launch it with the click of a button (only supported in Internet Explorer).
- **Zip File Handling**: If a `.zip` file containing an `.exe` is uploaded, the tool will extract and allow the `.exe` to be launched.
- **Browser Check**: The page checks whether the user is using Internet Explorer. If not, a warning modal is displayed.

## Requirements

- **Browser**: This tool is designed to work with **Internet Explorer** due to the usage of ActiveX to execute `.exe` files.
- **Operating System**: Should be used on a Windows machine that supports ActiveX controls.

## How to Use

1. **Open the HTML File**: Download the HTML file and open it in Internet Explorer.
2. **Select or Drag and Drop Files**:
    - Drag and drop an `.exe` file or a `.zip` file containing an `.exe` file into the designated drop area.
    - Alternatively, click the "Browse" button to select the file manually.
3. **Launch the Executable**:
    - After selecting an `.exe` file, the "Launch Executable" button will appear.
    - Click this button to execute the file.

   > **Note**: The executable will only run if you're using Internet Explorer. Other browsers will display a modal message informing the user that the action cannot be performed.

## How It Works

- The webpage uses **ActiveXObject** to execute the `.exe` file via the `WScript.Shell` API in Internet Explorer.
- **File Processing**: 
    - If the user uploads a `.zip` file, the contents are extracted and the `.exe` file is identified and made available for launching.
    - If a `.exe` file is uploaded directly, it will be selected and made ready to launch.

- The page contains modals for:
    - **Unsupported Browser**: If the browser is not Internet Explorer, it will show a modal prompting the user to continue anyway or close the page.
    - **Error**: Displays errors if something goes wrong during file handling or execution.
    - **Success**: Notifies the user if the executable is launched successfully.

## Known Issues

- **Internet Explorer Only**: This tool is limited to Internet Explorer due to the ActiveXObject usage. Modern browsers do not support this functionality.
- **Security Warning**: Running executables from untrusted sources may pose a security risk. Ensure the files are from a trusted origin before execution.

## Troubleshooting

- **No Executable Selected**: Ensure you have selected a valid `.exe` or `.zip` file containing an `.exe` file.
- **Failed to Launch Executable**: Check that ActiveX is enabled in Internet Explorer.
- **Unsupported Browser**: Use Internet Explorer to run this tool. Other browsers will not support the ActiveX functionality.

## Future Plans

In the future, we aim to extend the compatibility of this tool to modern browsers like **Chrome** and **Firefox**. The plan involves finding alternatives to **ActiveXObject**, such as leveraging WebAssembly or native browser extensions, to allow execution of `.exe` files directly within these modern environments. This would make the tool more accessible and usable across a wider range of browsers.

However, **Safari** will likely not support this functionality, as it does not provide support for ActiveX or any equivalent API for executing local executables. As a result, Safari users will not be able to launch `.exe` files via this tool.

## Contributing

Feel free to fork this repository, improve it, and submit pull requests. Any contributions to make it more robust or support more use cases are welcome!

## License

This project is open source and available under the MIT License. See the [LICENSE](LICENSE) file for more details.

## About XPDevs

This tool was developed and is maintained by **XPDevs**. XPDevs is committed to building simple, accessible software solutions with a focus on empowering users to make the most out of their systems. -> PAINT.EXE.

## Sample ZIP files

* https://lrusso.github.io/WinAppRunner/demos/paint.zip

* https://lrusso.github.io/WinAppRunner/demos/spider.zip

## Based on the work of:

https://github.com/danoon2/Boxedwine
