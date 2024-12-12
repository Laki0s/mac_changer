# 🛠️ Change_Mac

**Change_Mac** is a C application with a **GTK** graphical interface that allows you to:

- Display the current MAC address in real-time.
- Change the MAC address of a network interface.
- Restore the original MAC address.
- Use an intuitive graphical interface with buttons and text fields.

---

## 📦 Features

- **Display current MAC address**.
- **Easily change MAC address** via a text input field.
- **Quickly restore** the original MAC address.
- **GTK-based graphical interface**.

---

## 💻 Installation

### Prerequisites

Make sure you have the following libraries installed on your **Ubuntu** system:

```bash
sudo apt update && sudo apt upgrade
sudo apt install build-essential libgtk-3-dev pkg-config
```
## Compilation
Clone the repository and compile the program:

```bash
git clone https://github.com/Laki0s/change_mac.git
gcc -o mac_changer mac_changer.c `pkg-config --cflags --libs gtk+-3.0`
```

## 🚀 Usage
Run the program with root privileges and specify the network interface (e.g., eno1 or wlp4s0):
```bash
sudo ./mac_changer <interface>
```
Example:
```bash
sudo ./mac_changer eno1
```

## 📋 Network Interfaces
To find the name of your network interface, use the following command:
```bash
ip link
```
Sample output:
```sql
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1000
2: eno1: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP mode DEFAULT group default qlen 1000
3: wlp4s0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc noqueue state DOWN mode DORMANT group default qlen 1000
```
## ⚠️ Notes
- Root privileges are required to change the MAC address.
- If an interface is DOWN, you may need to set it UP before or after changing the MAC address.
- Use this tool responsibly and only on networks where you are authorized to change the MAC address.

## 🛠️ Troubleshooting
Common Issues
Error: gtk/gtk.h: No such file or directory
Solution: Install GTK 3:
```bash
sudo apt install libgtk-3-dev
```
Error: Usage: ./mac_changer <interface>
Solution: Ensure you specify an existing network interface, e.g.:
```bash
sudo ./mac_changer eno1
```

## 🤝 Contributing
Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a branch for your feature:
```bash
git checkout -b my-new-feature
```
3. Commit your changes:
```bash
git commit -m "Add my new feature"
```
4. Push to your fork
```bash
git push origin my-new-feature
```
5. Create a Pull Request.


## 📧 Contact
For any questions, reach out to me at: quentin.gehin@epitech.eu

## 🌟 If you like this project, give it a star on GitHub! 🌟
