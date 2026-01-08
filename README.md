# Uptime-robot-and-Uptime-kuma-and-how-to-use-it-in-on-our-application

### What is Uptime robot and Uptime kuma ?
Uptime robot and Uptime kuma both are website/service monitoring tools. Uptime robot is a cloud-based, beginner friendly and excelent for simple websites checks.
Uptime kuma is free and self hosted, open source application that offer more advanced features. Uptime-Kuma include ensuring website uptime, detecting outages, and monitoring server performance.


### To use Uptime robot...
To login create an account on their website. Then we can add the new monitor details.

### To use Uptime kuma...
To use this we need to self host. Here, I used kuma through docker container.

    sudo run -d --name kuma-moni \
    --restart=always \
    -p 3001:3001 \
    -v uptime-kuma:/app/data \
    louislam/uptime-kuma:1

**Here, -v          - Volume
      uptime-kuma - volume name
      /app/data   - dir inside the container**

### We can check the volume what we created, using this command

    sudo docker volume inspect uptime-kuma
