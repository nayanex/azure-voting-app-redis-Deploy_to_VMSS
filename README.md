# Local Environment Setup
### 1. **Install Redis** 
Download and install Redis server for your operating system: [Linux](https://redis.io/download), [MacOS](https://medium.com/@petehouston/install-and-config-redis-on-mac-os-x-via-homebrew-eb8df9a4f298), or [Windows](https://riptutorial.com/redis/example/29962/installing-and-running-redis-server-on-windows)

### 2. **Start Redis**
Start and verify the Redis server:
```bash
# Mac
redis-server /usr/local/etc/redis.conf
# Linux
redis-server
# Windows - Navigate to the Redis folder, and run
redis-server.exe
redis-cli.exe
# Ping your Redis server to verify if it is running. It will return "PONG"
redis-cli ping
```

### 3. **Create a Virtual Environment** (Optional)
It's your choice to work in a virtual environment. For this, you must have the [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html#via-pip) installed. Then, create and activate a virtual environment:
```bash
# Navigate to the azure-vote/ folder 
cd azure-vote/
```
```bash
# Mac/Linux
python3 -m venv .venv 
source .venv/bin/activate
# Windows on Powershell or GitBash terminal
py -3 -m venv .venv
.venv\Scripts\activate
```

### 4. **Dependencies**
Install dependencies from *requirements.txt*:
```bash
# Run this command from the parent directory where you have the requirements.txt file
pip install -r requirements.txt
``` 

### 5. Run the application:
```bash
# Navigate to the azure-vote/ folder if not already
cd azure-vote/
python main.py
```

>**NOTE**: The statement `app.run()` in `/azure-vote/main.py` file is currently set for your local environment. Replace it with the following statement when deploying the application to a VM Scale Set:
>```py
>app.run(host='0.0.0.0', threaded=True, debug=True)
>```
---
