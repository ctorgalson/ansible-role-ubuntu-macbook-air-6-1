# Macbook Air 6.1

This role corrects various small driver/compatibility issues and provides some power-management settings for the Macbook Air 6.1.

Under Ubuntu 16.10, the Air experiences a problem where the screen brightness will be zero after resume. This role includes a kernel module that corrects this issue.

## Role Variables

- `kernel_name`: name of the kernel module. Default: `mba6x_bl`
- `kernel_file_name`: file name of the file containing the module. Default: `mba6xbl-dkms_1.0.0_all.deb`.
- `powertop_commands`: a list of Powertop recommended commands to execute. Defaults:

  ```yaml
  powertop_commands:
    - "echo '1500' > '/proc/sys/vm/dirty_writeback_centisecs';"
    - "echo 'auto' > '/sys/bus/usb/devices/1-5/power/control';"
  ```

## License

MIT
