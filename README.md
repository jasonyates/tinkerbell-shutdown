# Tinkerbell Shutdown action

Tinkerbell action to shut down the host system by executing the ```poweroff``` command.

#### v0.0.1
Add action to your workflow, ```pid: host``` is required to allow the action to execute the ```poweroff``` command on the host.

Note: This will leave your workflow in ```STATE_RUNNING``` as the action does not cleanly exit.

```yaml
actions:
    - name: "Shutdown"
      image: docker.io/jasonyates07/tinkerbell-shutdown:0.0.1
      timeout: 90
      pid: host
```