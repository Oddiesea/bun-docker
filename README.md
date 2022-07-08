# bun-docker

A containerised Bun instance - An incredibly fast JavaScript runtime, bundler, transpiler and package manager – all in one. Check out the awesome Bun project [here](https://github.com/Jarred-Sumner/bun)

---

### Bun requires `io_uring` to work and this is disabled by default in docker, so either edit the default [secomp](https://raw.githubusercontent.com/docker/labs/master/security/seccomp/seccomp-profiles/default.json) profile to allow for this ( and run with container `--security-opt seccomp=/path/to/seccomp/profile.json` ) or simply run the container with ` seccomp=unconfined` - this is *NOT* recommended for production, read about more secomp and containers (including for k8s) [here](https://itnext.io/hardening-docker-and-kubernetes-with-seccomp-a88b1b4e2111]).