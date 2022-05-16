# Docker-Basic-Command

# Chack version
    docker version

# Docker image

    -- Create --
        docker build -t hello-docker

    -- see image created --
        docker images
    
    -- run --
        docker run <Image Name>

    -- Used to check which containers have been processed. -- 
        docker history ...

    -- Remove image --
     docker rmi <Image Name>

# Container

    -- View the details of the container. --
        docker inspect <CONTAINER_ID>

    -- View all containers that are running and that have stopped working. --
        docker ps -a

    -- Remove container --
        docker rm <ID Container>

# DockerFile command

    ENV : กำหนดตัวแปร environment ให้ตอนทำ image และ container

    ADD : copy file เข้า image

    COPY : copy file เข้า image ต่างกับ ADD ตรงที่ไฟล์ต้นฉบับได้เฉพาะ local เป็น remote url ไม่ได้

    ENTRYPOINT : คำสั่งที่จะให้ run หลังจาก start container

    VOLUME : กำหนด mount point ให้ image

    USER : กำหนด user ที่จะใช้ run คำสั่ง RUN CMD ENTRYPOINT

    WORKDIR : กำหนด working directory สำหรับ RUN CMD ENTRYPOINT COPY ADD

    ARG : กำหนดตัวแปรไว้สำหรับตอน BUILD

    ONBUILD : ใช้สำหรับให้ run คำสั่งแต่ให้รอ trigger เพื่อทำงานต่อในกรณีที่ต้องรอให้ build ตัวอื่นก่อน

    STOPSIGNAL : สั่งให้หยุดโดยใช้ system call signal

    SHELL : เปลี่ยนไปใช้ shell ที่กำหนด
    