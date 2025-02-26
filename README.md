# Quectel_MHI
 Quectel Linux Pcie Mhi driver

# Env
 ```
 yoki@ubuntu:/tmp/pcie_mhi$ uname -r
6.8.0-52-generic
yoki@ubuntu:/tmp/pcie_mhi$ lsb_release -d
No LSB modules are available.
Description:    Ubuntu 24.04.1 LTS
```

# Log
```
yoki@ubuntu:/tmp/pcie_mhi$ make
make ARCH=x86_64 CROSS_COMPILE= -C /lib/modules/6.8.0-52-generic/build M=/tmp/pcie_mhi clean
make[1]: Entering directory '/usr/src/linux-headers-6.8.0-52-generic'
make[1]: Leaving directory '/usr/src/linux-headers-6.8.0-52-generic'
find . -name *.o.ur-safe | xargs rm -f
make ARCH=x86_64 CROSS_COMPILE= -C /lib/modules/6.8.0-52-generic/build M=/tmp/pcie_mhi modules
make[1]: Entering directory '/usr/src/linux-headers-6.8.0-52-generic'
warning: the compiler differs from the one used to build the kernel
  The kernel was built by: x86_64-linux-gnu-gcc-13 (Ubuntu 13.3.0-6ubuntu2~24.04) 13.3.0
  You are using:           gcc-13 (Ubuntu 13.3.0-6ubuntu2~24.04) 13.3.0
  CC [M]  /tmp/pcie_mhi/core/mhi_init.o
/tmp/pcie_mhi/core/mhi_init.c:2694:6: warning: no previous prototype for ‘mhi_cntrl_exit’ [-Wmissing-prototypes]
 2694 | void mhi_cntrl_exit(void)
      |      ^~~~~~~~~~~~~~
  CC [M]  /tmp/pcie_mhi/core/mhi_main.o
/tmp/pcie_mhi/core/mhi_main.c:294:12: warning: no previous prototype for ‘mhi_to_physical’ [-Wmissing-prototypes]
  294 | dma_addr_t mhi_to_physical(struct mhi_ring *ring, void *addr)
      |            ^~~~~~~~~~~~~~~
/tmp/pcie_mhi/core/mhi_main.c:2590:5: warning: no previous prototype for ‘mhi_get_remote_time’ [-Wmissing-prototypes]
 2590 | int mhi_get_remote_time(struct mhi_device *mhi_dev,
      |     ^~~~~~~~~~~~~~~~~~~
  CC [M]  /tmp/pcie_mhi/core/mhi_pm.o
/tmp/pcie_mhi/core/mhi_pm.c:156:6: warning: no previous prototype for ‘mhi_assert_dev_wake’ [-Wmissing-prototypes]
  156 | void mhi_assert_dev_wake(struct mhi_controller *mhi_cntrl, bool force)
      |      ^~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/core/mhi_pm.c:196:6: warning: no previous prototype for ‘mhi_deassert_dev_wake’ [-Wmissing-prototypes]
  196 | void mhi_deassert_dev_wake(struct mhi_controller *mhi_cntrl, bool override)
      |      ^~~~~~~~~~~~~~~~~~~~~
  CC [M]  /tmp/pcie_mhi/core/mhi_boot.o
/tmp/pcie_mhi/core/mhi_boot.c:731:5: warning: no previous prototype for ‘BhiWrite’ [-Wmissing-prototypes]
  731 | int BhiWrite(struct mhi_controller *mhi_cntrl, void __user *ubuf, size_t size)
      |     ^~~~~~~~
/tmp/pcie_mhi/core/mhi_boot.c:821:6: warning: no previous prototype for ‘bhi_get_dev_info’ [-Wmissing-prototypes]
  821 | long bhi_get_dev_info(struct mhi_controller *mhi_cntrl, void __user *ubuf)
      |      ^~~~~~~~~~~~~~~~
/tmp/pcie_mhi/core/mhi_boot.c:840:6: warning: no previous prototype for ‘bhi_write_image’ [-Wmissing-prototypes]
  840 | long bhi_write_image(struct mhi_controller *mhi_cntrl, void __user *ubuf)
      |      ^~~~~~~~~~~~~~~
  CC [M]  /tmp/pcie_mhi/core/mhi_dtr.o
/tmp/pcie_mhi/core/mhi_dtr.c:272:6: warning: no previous prototype for ‘mhi_dtr_exit’ [-Wmissing-prototypes]
  272 | void mhi_dtr_exit(void) {
      |      ^~~~~~~~~~~~
  CC [M]  /tmp/pcie_mhi/controllers/mhi_qti.o
/tmp/pcie_mhi/controllers/mhi_qti.c:129:5: warning: no previous prototype for ‘mhi_debugfs_trigger_m0’ [-Wmissing-prototypes]
  129 | int mhi_debugfs_trigger_m0(void *data, u64 val)
      |     ^~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/controllers/mhi_qti.c:143:5: warning: no previous prototype for ‘mhi_debugfs_trigger_m3’ [-Wmissing-prototypes]
  143 | int mhi_debugfs_trigger_m3(void *data, u64 val)
      |     ^~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/controllers/mhi_qti.c:449:5: warning: no previous prototype for ‘mhi_system_suspend’ [-Wmissing-prototype]
  449 | int mhi_system_suspend(struct device *dev)
      |     ^~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/controllers/mhi_qti.c:1094:12: warning: no previous prototype for ‘mhi_controller_qcom_init’ [-Wmissing-prototypes]
 1094 | int __init mhi_controller_qcom_init(void)
      |            ^~~~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/controllers/mhi_qti.c:1099:6: warning: no previous prototype for ‘mhi_controller_qcom_exit’ [-Wmissing-prototypes]
 1099 | void mhi_controller_qcom_exit(void)
      |      ^~~~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/controllers/mhi_qti.c:1210:5: warning: no previous prototype for ‘mhi_arch_platform_init’ [-Wmissing-prototypes]
 1210 | int mhi_arch_platform_init(struct mhi_dev *mhi_dev)
      |     ^~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/controllers/mhi_qti.c:1215:6: warning: no previous prototype for ‘mhi_arch_platform_deinit’ [-Wmissing-prototypes]
 1215 | void mhi_arch_platform_deinit(struct mhi_dev *mhi_dev)
      |      ^~~~~~~~~~~~~~~~~~~~~~~~
  CC [M]  /tmp/pcie_mhi/devices/mhi_uci.o
/tmp/pcie_mhi/devices/mhi_uci.c:103:12: warning: no previous prototype for ‘user_termios_to_kernel_termios’ [-Wmissing-prototypes]
  103 | __weak int user_termios_to_kernel_termios(struct ktermios *k,
      |            ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/devices/mhi_uci.c:108:12: warning: no previous prototype for ‘kernel_termios_to_user_termios’ [-Wmissing-prototypes]
  108 | __weak int kernel_termios_to_user_termios(struct termios2 __user *u,
      |            ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/devices/mhi_uci.c:113:12: warning: no previous prototype for ‘user_termios_to_kernel_termios_1’ [-Wmissing-prototypes]
  113 | __weak int user_termios_to_kernel_termios_1(struct ktermios *k,
      |            ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/devices/mhi_uci.c:118:12: warning: no previous prototype for ‘kernel_termios_to_user_termios_1’ [-Wmissing-prototypes]
  118 | __weak int kernel_termios_to_user_termios_1(struct termios __user *u,
      |            ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/devices/mhi_uci.c:945:5: warning: no previous prototype for ‘mhi_device_uci_init’ [-Wmissing-prototypes]
  945 | int mhi_device_uci_init(void)
      |     ^~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/devices/mhi_uci.c:976:6: warning: no previous prototype for ‘mhi_device_uci_exit’ [-Wmissing-prototypes]
  976 | void mhi_device_uci_exit(void)
      |      ^~~~~~~~~~~~~~~~~~~
  CC [M]  /tmp/pcie_mhi/devices/mhi_netdev_quectel.o
/tmp/pcie_mhi/devices/mhi_netdev_quectel.c:79:5: warning: no previous prototype for ‘mhi_netdev_use_xfer_type_dma’ [-Wmissing-prototypes]
   79 | int mhi_netdev_use_xfer_type_dma(unsigned chan)
      |     ^~~~~~~~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/devices/mhi_netdev_quectel.c:213:5: warning: no previous prototype for ‘mhi_netdev_mbin_enabled’ [-Wmissing-prototypes]
  213 | int mhi_netdev_mbin_enabled(void) { return mhi_mbim_enabled; }
      |     ^~~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/devices/mhi_netdev_quectel.c:3393:12: warning: no previous prototype for ‘mhi_device_netdev_init’ [-Wmissing-prototypes]
 3393 | int __init mhi_device_netdev_init(struct dentry *parent)
      |            ^~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/devices/mhi_netdev_quectel.c:3407:6: warning: no previous prototype for ‘mhi_device_netdev_exit’ [-Wmissing-prototypes]
 3407 | void mhi_device_netdev_exit(void)
      |      ^~~~~~~~~~~~~~~~~~~~~~
/tmp/pcie_mhi/devices/mhi_netdev_quectel.c:3415:6: warning: no previous prototype for ‘mhi_netdev_quectel_avoid_unused_function’ [-Wmissing-prototypes]
 3415 | void mhi_netdev_quectel_avoid_unused_function(void) {
      |      ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  LD [M]  /tmp/pcie_mhi/pcie_mhi.o
  MODPOST /tmp/pcie_mhi/Module.symvers
  CC [M]  /tmp/pcie_mhi/pcie_mhi.mod.o
  LD [M]  /tmp/pcie_mhi/pcie_mhi.ko
  BTF [M] /tmp/pcie_mhi/pcie_mhi.ko
Skipping BTF generation for /tmp/pcie_mhi/pcie_mhi.ko due to unavailability of vmlinux
make[1]: Leaving directory '/usr/src/linux-headers-6.8.0-52-generic'
#cp pcie_mhi.ko /tftpboot/
yoki@ubuntu:/tmp/pcie_mhi$ ls
controllers  devices  Makefile       Module.symvers  pcie_mhi.mod    pcie_mhi.mod.o  README
core         log      modules.order  pcie_mhi.ko     pcie_mhi.mod.c  pcie_mhi.o      ReleaseNote.txt
yoki@ubuntu:/tmp/pcie_mhi$
```
