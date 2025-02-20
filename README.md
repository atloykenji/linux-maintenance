## Nice to Know Commands 😉

- **neofetch**: ASCII display of system info.  
- **htop**: System monitor.  
- **-k**: Kill process.  
- **clear**: Clears the terminal.  
- **exit**: Exit the terminal session.  
- **ping 1.1.1.1**: Check connection.
-  **history**: View the history of previously run commands.

---

## Basic Commands:

- **cd**: Change directory (e.g., `cd bash.history`).  
- **ls -lh**: Long-format list of files.  
- **xdg-open**: Open files (e.g., go to file location using `cd` and `xdg-open ado-1648663676344-142.jpg`).  
- **ls**: List directories (most frequently used command).  
- **pwd**: Print working directory.  
- **mkdir**: Create directories.  
- **mv**: Move or rename files.  
- **cp**: Copy files.  
- **rm**: Delete files or directories.  
- **touch**: Create blank/empty files.  
- **ln**: Create symbolic links (shortcuts).  
- **cat**: Display file contents.  
- **clear**: Clear the terminal display.  
- **echo**: Print any text that follows the command.  
- **less**: Display paged outputs in the terminal.  
- **man**: Access manual pages for Linux commands.  
- **uname**: Get basic information about the OS.  
- **whoami**: Get the active username.  
- **tar**: Extract and compress files.  
- **grep**: Search for a string within an output.  
- **head**: Return specified lines from the top.  
- **tail**: Return specified lines from the bottom.  
- **diff**: Find the difference between two files.  
- **cmp**: Check if two files are identical.  
- **comm**: Combine the functionality of `diff` and `cmp`.  
- **sort**: Sort file content while outputting.  
- **export**: Export environment variables.  
- **zip**: Zip files.  
- **unzip**: Unzip files.  
- **ssh**: Secure Shell command.  
- **service**: Start and stop services.  
- **ps**: Display active processes.  
- **kill / killall**: Kill active processes by process ID or name.  
- **df**: Display disk filesystem info.  
- **mount**: Mount file systems.  
- **chmod**: Change file permissions. Example: **chmod 777 [file]**: Give full permissions to a file or directory.
- **chown**: Change ownership of files or folders.  
- **ifconfig**: Display network interfaces and IPs.  
- **traceroute**: Trace network hops to a destination.  
- **wget**: Download files from the internet.  
- **ufw**: Firewall command.  
- **iptables**: Base firewall utility.  
- **apt, pacman, yum, rpm**: Package managers (depending on the distro).  
- **sudo**: Escalate privileges.  
- **cal**: View a command-line calendar.  
- **alias**: Create custom shortcuts for commands.  
- **dd**: Create bootable USB sticks.  
- **whereis**: Locate binary, source, and manual pages for a command.  
- **whatis**: Find what a command does.
- **find [path] -name [filename]**: Search for files by name in a directory.
- **top**: View live active processes and system usage.  
- **useradd / usermod**: Add new users or modify existing ones.  
- **passwd**: Create or update user passwords.
- **iostat**: Display CPU and I/O statistics.
- **mount -o loop [image-file] /mnt**: Mount an ISO file or disk image as a loopback device.
- **umount [device]**: Unmount a mounted device or filesystem.
- **ip a**: Show all IP addresses on the system.
- **curl -I [URL]**: Get the HTTP headers from a URL.
---

## Shutdown and Reboot Commands:

- **shutdown -h now**: Explicit halt and power-off the system immediately.  
- **shutdown -P now**: Explicitly tells the system to power off.  
- **sudo shutdown -r now**: Safely shuts down and immediately reboots the system.  
- **reboot**: Directly reboots the system.  
- **systemctl reboot**: Reboot using `systemd` (preferred).

---

## Package Management (Debian/Ubuntu Specific):

- **sudo apt update**: update archives.
- **sudo apt upgrade**: update packages.
- **sudo apt-get install --only-upgrade google-chrome-stable**: to only upgrade package (dont use chrome).
- **sudo apt update && sudo apt upgrade**: update all (or use this **sudo apt update && sudo apt upgrade -y**)
- **apt-cache search [package]**: Search for a package in the apt repository.
- **apt-get dist-upgrade**: Perform a distribution upgrade, handling dependency changes.
- **apt autoclean**: free up space by removing obsolete packages but still want to keep currently valid ones
- **apt autoremove**: periodically to clean up unnecessary packages
- **sudo apt clean**: Clear the local package cache to fix issues caused by corrupted cache files.
- **sudo apt-get install --reinstall [package]**: Reinstall a package if it’s causing errors
- **sudo apt-get update --fix-missing**: Fix missing package errors when updating packages.
- **sudo apt --fix-broken install**: Fix broken package installations or dependencies.
- **sudo dpkg --configure -a**: Configure packages that were unpacked but not yet configured.

## Package Management (Arch-Specific)
In Arch-based distros, pacman is used instead of apt.

- sudo pacman -Syu → Update system (equivalent to apt update && apt upgrade).
- sudo pacman -S [package] → Install a package.
- sudo pacman -Q → List installed packages.
- sudo pacman -Qs [package] → Search for installed packages.
- sudo pacman -Ss [package] → Search for available packages in repos.
- sudo pacman -U /path/to/package.pkg.tar.zst → Install a local package file.
- sudo pacman -R [package] → Remove package (keep dependencies)
- sudo pacman -Rns [package] →  Remove package + dependencies + config
- sudo pacman -Sc → Remove unused package cache.
- sudo pacman -Scc → Delete all cached packages.
- yay -Syu → Update AUR and official packages
- yay -S [package] → Install an AUR package.
- yay -Ss [package] → Search in AUR
- yay -Rns [package] → Remove an AUR package and its dependencies.

- sudo reflector --latest 5 --sort rate --save /etc/pacman.d/mirrorlist →  Managing mirrors (faster downloads)
---

## Errors and Troubleshooting:

- **kill audioprocess -   pulseaudio -k**: For audio driver/device  not detecting...and then run pulseaudio again.
- **sudo service network-manager restart**: restart the network manager service.(systemctl restart NetworkManager for arch-based)
- **sudo lshw -C network**: Check hardware details for network interfaces (helps in identifying network issues).
- **sudo systemctl restart [service]**: Restart a system service if it is not functioning
- **sudo systemctl restart gdm**: Restart the GDM display manager if graphical interface fails to load.(Other distros may use sddm, lightdm, or xdm.) 
- **sudo systemctl restart graphical.target**: Restart the graphical target to resolve graphical interface issues.
- **xrandr --auto**: Automatically detect and configure connected monitors (helpful if a second monitor isn't being detected).
- **journalctl -xe**: View system logs for errors.
- **fsck /dev/sda1**: Check and repair a filesystem (replace /dev/sda1 with the correct partition) if there are disk errors.
