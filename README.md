🍀 Clover Client

Clover is a modern and customizable Minecraft client designed to enhance gameplay with a wide range of quality-of-life features. Built on the Fabric modding platform, Clover focuses on performance, flexibility, and an intuitive user experience while remaining lightweight and easy to install.

✨ Features
Modular Design – Enable or disable features to suit your playstyle.
Enhanced Movement – Improved navigation and traversal options.
Combat Assistance – Tools that provide smoother and more responsive engagements.
World & Exploration Utilities – Increased environmental awareness and efficiency.
Performance Optimizations – Lightweight and optimized for stable gameplay.
Clean GUI – User-friendly interface with extensive configuration options.
Regular Updates – Continuous improvements and new features.
📦 Requirements

Before installing Clover, ensure you have the following:

Minecraft: Java Edition
Java 17 or newer
Fabric Loader
Fabric API
🔗 Useful Links
Fabric Loader: https://fabricmc.net/use/installer/
Fabric API (CurseForge): https://www.curseforge.com/minecraft/mc-mods/fabric-api
Fabric API (Modrinth): https://modrinth.com/mod/fabric-api
🛠️ Installation Guide
Step 1: Install Fabric Loader
Download the Fabric Installer from the official website.
Run the installer.
Select the Minecraft version compatible with Clover.
Ensure "Install Client" is selected.
Click Install.
Launch the Minecraft Launcher and verify that a Fabric profile appears.
Step 2: Install Fabric API
Download the latest version of Fabric API matching your Minecraft version.
Navigate to your Minecraft mods folder:

Windows:

%appdata%\.minecraft\mods

macOS:

~/Library/Application Support/minecraft/mods

Linux:

~/.minecraft/mods
If the mods folder does not exist, create it.
Place the downloaded Fabric API .jar file into the mods folder.
Step 3: Install Clover
Download the latest release of Clover from the repository’s Releases page.
Place the Clover-x.x.x.jar file into the same mods folder.
Ensure both Fabric API and Clover are present in the folder.
Step 4: Launch the Game
Open the Minecraft Launcher.
Select the Fabric profile.
Click Play.
Once in-game, Clover should initialize automatically.
🎮 Getting Started
Opening the GUI
Press Right Shift (default key) to open the Clover interface.
Keybinds can be customized within the settings menu.
Enabling Features
Open the GUI.
Navigate through the available categories.
Toggle modules on or off as desired.
Adjust settings to personalize your experience.
Configuration

Clover automatically generates a configuration folder on first launch:

.minecraft/config/clover/
Settings are saved between sessions.
Profiles can be backed up or shared.
🔄 Updating Clover
Download the latest version from the Releases page.
Replace the old .jar file in the mods folder with the new one.
Restart Minecraft to apply the update.
❗ Troubleshooting
Game Crashes on Launch
Ensure you are using Java 17 or newer.
Verify that the Minecraft, Fabric Loader, and Fabric API versions match.
Remove any conflicting mods and try again.
Check the logs/latest.log file for detailed error information.
Clover Not Appearing In-Game
Confirm that the .jar file is placed in the correct mods folder.
Make sure the Fabric profile is selected in the launcher.
Ensure Fabric API is installed.
Performance Issues
Allocate more RAM to Minecraft via the launcher.
Disable unnecessary mods.
Update graphics drivers.
Consider using performance-enhancing mods such as Sodium (optional).
📁 Project Structure
Clover/
├── src/
├── gradle/
├── build.gradle
├── settings.gradle
├── LICENSE
└── README.md
🤝 Contributing

Contributions are welcome and appreciated.

Fork the repository.

Create a new branch:

git checkout -b feature/YourFeature

Commit your changes:

git commit -m "Add: Description of feature"

Push to your fork:

git push origin feature/YourFeature
Open a Pull Request describing your changes.
📜 License

This project is licensed under the GNU General Public License v3.0 (or your chosen license). See the LICENSE file for more details.

⚠️ Disclaimer

Clover is intended for educational and experimental purposes. Users are responsible for ensuring compliance with the terms of service of any servers they join. The developers assume no liability for misuse or potential consequences resulting from its use.

💬 Support
Issues: Use the GitHub Issues tab to report bugs or request features.
Discussions: Join the community to share feedback and ideas.
🌟 Acknowledgments
The Fabric team for their robust and lightweight modding platform.
The Minecraft modding community for continuous inspiration and support.
