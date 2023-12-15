# Setting Up Code Compiler with Judge0

Follow these steps to set up Judge0 for code compilation.

## 1. Clone the Judge0 Repository

```bash
git clone https://github.com/judge0/judge0.git
cd judge0-v1.13.0
```

## 2. Start Database and Redis Services

```bash
docker-compose up -d db redis
```

## 3. Start Judge0 Services

```bash
docker-compose up -d
```

## 4. Configure Docker Settings

Edit the Docker settings file using Vim:

```bash
vim ~/Library/Group\ Containers/group.com.docker/settings.json
```

Append the following line to enable the deprecatedCgroupv1:

```bash
"deprecatedCgroupv1": true
```

Save the file and exit Vim.

## 5. Restart Docker

```bash
sudo pkill Docker
open /Applications/Docker.app
docker restart [containerID1] [containerID2] [containerID3] [containerID4]
```

Replace [containerID] with the actual ID of the Docker container.

## 6. Access the Judge0 Site

Visit http://0.0.0.0:2358/dummy-client.html in your web browser to access the Judge0 site.

Now you should have Judge0 set up for code compilation. Enjoy coding!
