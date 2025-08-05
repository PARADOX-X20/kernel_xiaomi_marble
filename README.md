
## 📱 Device Information

- **Device**: Xiaomi Poco F5 (marble)
- **Codename**: marble
- **Maintainer**: [PARADOX_X20](https://github.com/PARADOX-X20)
- **Status**: ✅ **FULLY FUNCTIONAL** - Nethunter Kernel Successfully Booted!

## 🎯 About This Project

This is a **custom Nethunter kernel** for the Poco F5 device specifically designed to support **Kali NetHunter**, the world's most advanced penetration testing platform for Android devices. The kernel includes comprehensive security and penetration testing features required for NetHunter functionality.

## 📋 Requirements

- **Android Version**: Android 13+ (AOSP/LineageOS)
- **Recovery**: TWRP or compatible custom recovery
- **Unlocked Bootloader**: Required for custom kernel installation
- **NetHunter App**: Kali NetHunter application installed

## 🚀 Installation

### Prerequisites
1. Unlock your device bootloader
2. Install a compatible custom recovery (TWRP recommended)
3. Install Kali NetHunter application from the official store
4. Backup your current kernel (recommended)

### Installation Steps
1. Download the latest kernel zip file
2. Boot into recovery mode
3. Flash the kernel zip file
4. Clear dalvik cache (optional but recommended)
5. Reboot to system
6. Configure NetHunter settings

## 🔄 Updates

- **✅ STABLE RELEASE**: Kernel is fully functional and tested
- **Regular Updates**: Kernel updates are released periodically
- **Security Patches**: Latest security patches included
- **Feature Additions**: New NetHunter features added regularly

## 🛠️ Building from Source

### Prerequisites
- Linux environment (Ubuntu 20.04+ recommended)
- Android build tools
- Device tree and vendor blobs
- AOSP/LineageOS source tree (for toolchain)

### Quick Build (Recommended)
Use the provided `build.sh` script for easy compilation:

```bash
# Clone the repository
git clone https://github.com/PARADOX-X20/kernel_xiaomi_marble.git
cd kernel_xiaomi_marble

# Make build script executable
chmod +x build.sh

# Build for Poco F5 (marble)
./build.sh marble

# Clean build (optional)
./build.sh -c marble

# Build without LTO (optional)
./build.sh

# Only generate config (optional)
./build.sh
```

### Build Script Options
- `-c, --clean`: Clean build directory before building
- `-n, --no-lto`: Disable Link Time Optimization
- `-o, --only-config`: Only generate kernel config
- `marble`: Target device (Poco F5 codename)

### Manual Build Instructions
For advanced users who want to build manually:

```bash
# Clone the repository
git clone https://github.com/PARADOX-X20/kernel_xiaomi_marble.git
cd kernel_xiaomi_marble

# Set up build environment
export ARCH=arm64
export SUBARCH=arm64
export CROSS_COMPILE=aarch64-linux-android-

# Configure kernel
make defconfig

# Build kernel
make -j$(nproc)

# Generate flashable zip
# (Additional steps required for packaging)
```

## 📞 Support & Contact

### Maintainer
- **GitHub**: [@PARADOX-X20](https://github.com/PARADOX-X20)
- **Telegram**: [@PARADOX_X20](https://t.me/PARADOX_X20)

## ⚠️ Disclaimer

- This kernel is for educational and security testing purposes
- Use responsibly and only on devices you own
- The maintainer is not responsible for any damage to your device
- Always backup your data before flashing custom kernels

---

**✅ STATUS**: This kernel is **FULLY FUNCTIONAL** and has been successfully tested on Poco F5. All Nethunter features are working properly.

**⚠️ Important**: This kernel is specifically designed for security testing and penetration testing purposes. Please use responsibly and in accordance with applicable laws and regulations.

**🚀 Ready for Production Use!** 🎉
