# Command walkthrough

Run commands individually inside Linux, not Windows PowerShell.
Use a fresh lab with no existing /app directory. Replace mcebisi with your own Linux username. sudo requests your Linux password; characters are not shown while typing.

## 1. Identify the user and location

```bash
whoami
cd ~
pwd
ls -la
```

## 2. Create folders and set ownership

```bash
sudo mkdir -p /app/logs
sudo chown -R mcebisi:mcebisi /app
ls -ld /app /app/logs
```

The ownership change was a lab setup step so subsequent file operations could run without sudo.

## 3. Create the configuration placeholder

```bash
touch /app/config.conf
ls -l /app/config.conf
```

Expected on a fresh run: an empty file with a size of 0 bytes.

## 4. Create and read the log

```bash
echo "Started" > /app/logs/server.log
cat /app/logs/server.log
```

Expected text: Started. The > operator overwrites existing file contents.

## 5. Verify the structure

```bash
pwd
ls -R /app
```

## 6. Rename the log and inspect permissions

```bash
mv /app/logs/server.log /app/logs/server.bak
ls -l /app/config.conf
ls -R /app
cat /app/logs/server.bak
```

Observed configuration permissions in my session: -rw-r--r--.
Final log filename: server.bak. Final log contents: Started.

