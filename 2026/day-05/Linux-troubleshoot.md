## Target Service / Process

* **Service:** Docker (`docker.service`)
* **Daemon PID:** 2262
* **Status:** Active / Running


## Snapshot: CPU & Memory

* **CPU usage:** 0.0% (daemon idle)
* **Memory usage:** 8.7% of total RAM



## Snapshot: Disk & I/O

* **Root filesystem usage:** 37% (2.5G used of 6.8G)
* **/var/log size:** 17M


## Snapshot: Network

* **Docker socket:** No TCP ports found for Docker daemon (`dockerd`) — since it uses a Unix socket
* **Container connectivity:** `/ping` endpoint returns HTTP 200 OK



## Logs Reviewed

* Docker startup logs: Daemon initialized successfully, API listening on socket.
* Images pulled (`nginx:latest`, `httpd:latest`), containers attached to networks.



## Quick Findings

* Docker daemon stable and running.
* System resources (CPU, memory, disk) healthy.
* Container networking working as expected.
* No major errors in logs affecting service operation.

## If This Worsens

1. **Monitor & Limit Resources:** Use `docker stats` and set CPU/memory limits on containers.
2. **Investigate Logs:** Check `journalctl -u docker -f` and `docker logs <container-id>` for errors.
3. **Restart / Scale Services:** Restart problematic containers or update services with `docker service update --force <service>`; scale nodes if needed.
