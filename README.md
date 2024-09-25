## How to Install and Run Node-RED on Debian (Short Guide)

This guide provides a concise walkthrough for installing and running Node-RED on any Debian version (9, 10, 11, 12).

**Prerequisites:**

* Debian installed and configured.
* Node.js runtime >=14.16.

**Steps:**

1. **Update Debian:**
   ```bash
   sudo apt update
   sudo apt upgrade -y
   ```

2. **Install Node.js:**
   ```bash
   curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -
   sudo apt-get install nodejs -y
   ```

3. **Install Node-RED:**
   ```bash
   sudo npm install -g --unsafe-perm node-red
   ```

4. **Run Node-RED:**
   ```bash
   node-red
   ```

5. **Access Node-RED:** Open your web browser and navigate to `http://localhost:1880`.

6. **(Optional) Run Node-RED as a Service:**
   ```bash
   sudo npm install -g pm2
   pm2 start `which node-red` -- -v
   pm2 save
   pm2 startup
   ```

**Note:** Replace `18.x` in step 2 with your desired Node.js version (>=14.16).

That's it! You now have a running Node-RED server on your Debian machine. Enjoy! 
