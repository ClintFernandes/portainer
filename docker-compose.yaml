version: "3.5"
services:
    portainer_web:
        image: portainer/portainer-ce:2.19.4
        container_name: portainer_web
        command: -H unix:///var/run/docker.sock
        ports:
          - 9000:9000
          - 9443:9443
        volumes:
          - /var/run/docker.sock:/var/run/docker.sock
          - portainer_web:/data
        restart: unless-stopped
        networks:
          - portainer

volumes:
    portainer_web:
        driver: local
        name: portainer_web

networks:
    portainer:
        name: portainer
