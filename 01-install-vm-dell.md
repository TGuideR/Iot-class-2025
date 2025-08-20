# 📄 Debian Installation Report for IoT, MQTT, Kafka Course

> Students must complete all sections of this form during Debian installation and submit it upon completion.

---

## 🔧 General Information

| Title                  | Value                                               |
| -----------------------| --------------------------------------------------- |
| Full Name              | Thanakorn Rakkam|
| Student ID              | 6510301046|
| Installation Date      | 11/06/2025|


---

## 🖥️ Device Information

- 💻 **Device Model / Type**: DELL Edge Gateway 5000
- 🧬 **Firmware Type**:  
  - [ ] UEFI  
  - [x] BIOS  
- 🏷️ **Installation Type**:  
  - [x] Physical PC  
  - [ ] Virtual Machine (VM)

---

## 🗂️ Custom Partitioning

| Partition      | Size   | Filesystem | Mount Point         | Notes                      |
|----------------|--------|------------|----------------------|----------------------------|
| `/dev/sda1`     | 29GB   | ext4       | `/`                  | Root filesystem            |
| `udev`          | 1.9GB  | tmpfs      | `/dev`               | Device files               |
| `tmpfs`         | 379MB  | tmpfs      | `/run`               | Runtime data               |
| `tmpfs`         | 1.9GB  | tmpfs      | `/dev/shm`           | Shared memory              |
| `tmpfs`         | 5MB    | tmpfs      | `/run/lock`          | Lock files                 |
| `tmpfs`         | 379MB  | tmpfs      | `/run/user/1000`     | User-specific runtime data |


---

## 🌐 Network Configuration (Static IP)

| Title                   | Value                                               |
| ------------------------| --------------------------------------------------- |
| Network Interface Name  | enp1|
| IP Address              | 172.30.15.47|
| Netmask                 | 255.255.255.0|s0
| Gateway                 | 172.30.15.254|
| DNS                     | 172.16.46.254|

---

## 🖧 Hostname

- 🖥️ **Hostname Set**: FDT6510301046

---

## 👤 User Account

- 👨‍💻 **Username Created**: Thanakorn
- 🔐 **Is a Root Password Set?**:  
  - [X] Yes  
  - [ ] No

---

## ✅ Additional Problems Notes (if any)

> _____________________________________________________________________  
> _____________________________________________________________________  
> _____________________________________________________________________

