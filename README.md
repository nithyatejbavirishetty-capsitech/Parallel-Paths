# 🎮 Parallel Paths – Android Signing Configuration

This document contains the **release keystore configuration details** for the *Parallel Paths* game.  
Keep this information secure and backed up — it is required for future updates and integrations.

---

## 🔐 Keystore Details

- **Keystore File**: `parallelpaths-release.jks`  
- **Keystore Password**: `parallelpaths`  
- **Alias (Key Name)**: `parallelpaths`  
- **Key Password**: `parallelpaths`  

---

## 🔑 Certificate Fingerprints

### SHA-1
62:58:F9:3C:43:43:C3:8B:B3:8B:0D:18:DD:90:CD:3E:1C:5A:AB:BC

### SHA-256
A3:BE:75:E0:F1:62:04:AA:30:69:A0:92:07:EB:7C:2B:06:AC:9F:66:46:47:4D:B2:2C:48:54:64:7F:56:0F:EA

---

## 📦 Godot Configuration

Go to:

Project → Export → Android → Signing

Fill the following:

- **Keystore** → Path to `parallelpaths-release.jks`  
- **User (Alias)** → `parallelpaths`  
- **Password** → `parallelpaths`  

##

---

## 🔧 Keystore Generation & SHA Fingerprints

### 1) Generate Release Keystore

keytool -genkey -v -keystore parallelpaths-release.jks -keyalg RSA -keysize 2048 -validity 10000 -alias parallelpaths-key

### 2) Get SHA's

keytool -list -v -keystore parallelpaths-release.jks -alias parallelpaths-key