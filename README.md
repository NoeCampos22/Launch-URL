[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/NoeCampos22/Launch-URL">
    <img src="repo_assets/logo.svg" alt="Logo" width="80" height="80">
    
  </a>

  <h3 align="center">Launch-URLs</h3>

  <p align="center">
    Easily create .desktop files to open URLs from your application menu, dock or dash.
    <br />
    ·
    <a href="https://github.com/NoeCampos22/Launch-URL/issues">Report Bug</a>
    ·
    <a href="https://github.com/NoeCampos22/Launch-URL/issues">Request Feature</a>
    ·
  </p>
</p>
<br />


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li><a href="#project-description">Project Description</a></li>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#usage">Usage</a>
    <ul>
        <li><a href="#open-as-a-tab">Open as a Tab</a></li>
        <li><a href="#open-as-an-app">Open as an App</a></li>
      </ul>
    </li>
    <li><a href="#future-features-and-issues">Future Features and Issues</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact-info">Contact Info</a></li>
  </ol>
</details>
<br />

<!-- Project Description -->
## Project Description

Sometimes we visit a web page so many times that even open it from the web browser's bookmark is not fast enough. Or it may be the case of wanting to open a webpage separate from all the other tabs, as if it were its own application.

Launch-URLs takes advantage that in Linux you can create .desktop files to execute a command. Makes easier the procces of creating one that opens URLs on the browser **(NOTE: At the moment, it is compatible/tested just with Brave Browser)**. Also, it adds the option of opening URLs as if they were an independent application, which does not create new instances each time it is executed but brings the already open tab to the front of the screen.

![Initial Demo!](repo_assets/initial_demo.gif)
<br />


<!-- INSTALLATION -->
## Installation
Follow the next steps to download and install correctly the script.

1. Clone the repo
   ```sh
   git clone https://github.com/NoeCampos22/Launch-URL.git
   ```
2. Enter the repo directory and run the install script
   ```sh
   cd Launch-URL
   ./install -Y # The -Y option is to install automatically the dependencies
   ```

**Note:** By default, the script will be installed on the /usr/bin/ directory, but, it can be specified a different directory (it must be on the $PATH variable) with the --path option.
<br />


<!-- USAGE EXAMPLES -->
## Usage
Now that it is already installed is time to create new .desktop files!
<br />

### Open as a Tab
With this option you will be able to create a .desktop file that opens the url on new tab each time is executed. For example, if you want to make a .deskfile that opens Youtube:

   ```sh
   # LaunchURLs --deskfile --asTab "Deskfile Name" "URL"
   LaunchURLs --deskfile --asTab "Youtube" "https://www.youtube.com/"
   ```

After that, you need to log out and log in, for the application menu to update.

![Open as a Tab!](repo_assets/as_tab.gif)
<br/>

### Open as an app
With this option the .desktop files you create will open the url on a new window, which do not have the search bar and bookmarks. It will also keep track of the window to bring it upfront each time the file is executed. 
The next example shows how to create a file that opens Notion on a page named Example:

   ```sh
   # LaunchURLs --deskfile --asApp "Deskfile Name" "URL" "Window Name"
   LaunchURLs --deskfile --asApp "Notion" "notion.so/Example" "Example"
   ```

To get the *Window Name*, open a terminal and follow the next steps:

   ```sh
   # 1. Open the url as an app
   brave-browser --app=https://www.notion.so/Example
   # 2. Wait for it to finish loading
   # 3. List all the windows. On the last column it will be the windows name, copy the one you need.
   wmctrl -l 
   ```

After that, you need to log out and log in, for the application menu to update.

![Open as a App!](repo_assets/as_app.gif)
<br />

### Important Notes
1. In both options, For the deskfile to have an icon, it must be downloaded (as .png or .svg) and copied to the /usr/share/icons directory with the exact same name as the Deskfile Name and without extension.
    ```sh
    sudo cp Deskfile_Name.png /usr/share/icons/Deskfile_Name
    ```

2. Right now, the script it is only tested and made to work with Brave Browser. So you are welcomed to fork the repo and modify it to work with your daily browser and even contribute, since it is planned to implement the option to work with other browsers.

3. This script was developed and only tested on Ubuntu 20.04. But it should be compatible with many other previous and future versions since its developed with just built-in bash code and has the only one dependency.
<br />


<!-- Future Features & Issues -->
## Future Features and Issues

See the [open issues](https://github.com/NoeCampos22/Launch-URL/issues) for a list of proposed features (and known issues).
<br />


<!-- CONTRIBUTING -->
## Contributing
I am always open to contribution: solving issues, implementing new features or improving current code. Please follow the next steps to make a contribution:

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/GreatContribution`)
3. Commit your Changes (`git commit -m 'Add some Great Contribution'`)
4. Push to the Branch (`git push origin feature/GreatContribution`)
5. Open a Pull Request
<br />


<!-- LICENSE -->
## License
Distributed under the MIT License. See [LICENSE](LICENSE.md) for more information.
<br />


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/NoeCampos22/repo.svg?style=for-the-badge
[contributors-url]: https://github.com/NoeCampos22/repo/graphs/contributors

[forks-shield]: https://img.shields.io/github/forks/NoeCampos22/repo.svg?style=for-the-badge
[forks-url]: https://github.com/NoeCampos22/repo/network/members

[stars-shield]: https://img.shields.io/github/stars/NoeCampos22/repo.svg?style=for-the-badge
[stars-url]: https://github.com/NoeCampos22/repo/stargazers

[issues-shield]: https://img.shields.io/github/issues/NoeCampos22/repo.svg?style=for-the-badge
[issues-url]: https://github.com/NoeCampos22/repo/issues

[license-shield]: https://img.shields.io/github/license/NoeCampos22/repo.svg?style=for-the-badge
[license-url]: https://github.com/NoeCampos22/repo/blob/master/LICENSE.txt