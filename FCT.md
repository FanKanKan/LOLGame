FCT debug command definition file
=================================


Version Info
------------
2017/11/13       Initial Release


Commands
=================================
test
----------
- CommandName:`test`
- Command2Send:`TerminalBlock@ping -c 4 {{HOSTNAME}}`

zynqversion
----------
- CommandName:`zynqversion`
- Command2Send:`Zynq@[123]version(0)`

poweron
----------
- CommandName:`poweron`
- Command2Send:`Zynq@[123]io set(1,bit51=0)`
- Command2Send:`Zynq@[123]io set(1,bit96=1)`
- Command2Send:`Zynq@[123]io set(9,bit111=1,bit110=0,bit109=0,bit112=1,bit89=1,bit75=1,bit83=0,bit73=1,bit74=0)`

poweroff
----------
- CommandName:`poweroff`
- Command2Send:`Zynq@[123]io set`

monitorpch
----------
- CommandName:`monitorpch`
- Command2Send:`Zynq@[123]io set(2,bit33=1,bit26=1)`
- Command2Send:`TerminalBlock@nc -c ${{HOSTNAME}} 7603`

potassiumdebug
----------
- CommandName:`potassiumdebug`
- Command2Send:`Zynq@[123]io set(5,bit121=1,bit67=0,bit46=1,bit32=1,bit31=1)`
- Command2Send:`TerminalUnBlock@nanocom -d \`
- Command2Send:`TerminalBlock@nc -4 -u localhost 31337`

chimpdebug
----------
- CommandName:`chimpdebug`
- Command2Send:`TerminalBlock@astrisctl relay dbgfifo 1`
- Command2Send:`TerminalBlock@astrisctl relay hippochannels 1`
- Command2Send:`TerminalUnblock@nanocom -h`
- Command2Send:`TerminalBlock@nc -4 -u localhost 31337`

xareset211
----------
- CommandName:`xareset211`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0D)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,01)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,02)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,03)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,06)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,11)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`

xbreset211
----------
- CommandName:`xbreset211`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0D)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,01)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,02)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,03)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,06)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,11)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`

tareset211
----------
- CommandName:`tareset211`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0D)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,01)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,02)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,03)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,06)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,11)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`

tbreset211
----------
- CommandName:`tbreset211`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0D)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,01)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,02)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,03)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,06)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,11)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`

xausb2.0_top
----------
- CommandName:`xausb2.0_top`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,01)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`

xausb2.0_bot
----------
- CommandName:`xausb2.0_bot`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,02)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`

xausb3.0_top
----------
- CommandName:`xausb3.0_top`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,03)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`

xausb3.0_bot
----------
- CommandName:`xausb3.0_bot`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,06)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x38,6,08,04,47,50,73,6c)`

xbusb2.0_top
----------
- CommandName:`xbusb2.0_top`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,01)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`

xbusb2.0_bot
----------
- CommandName:`xbusb2.0_bot`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,02)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`

xbusb3.0_top
----------
- CommandName:`xbusb3.0_top`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,03)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`

xbusb3.0_bot
----------
- CommandName:`xbusb3.0_bot`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,06)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_1,0x39,6,08,04,47,50,73,6c)`


tausb2.0_top
----------
- CommandName:`tausb2.0_top`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,01)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`

tausb2.0_bot
----------
- CommandName:`tausb2.0_bot`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,02)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`

tausb3.0_top
----------
- CommandName:`tausb3.0_top`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,03)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`

tausb3.0_bot
----------
- CommandName:`tausb3.0_bot`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,06)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x38,6,08,04,47,50,73,6c)`

tbusb2.0_top
----------
- CommandName:`tbusb2.0_top`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,01)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`

tbusb2.0_bot
----------
- CommandName:`tbusb2.0_bot`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,02)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`

tbusb3.0_top
----------
- CommandName:`tbusb3.0_top`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,03)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`

tbusb3.0_bot
----------
- CommandName:`tbusb3.0_bot`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,08)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,07)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,06)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0C)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0E)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,10)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,0F)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,68)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,3,09,01,00)`
- Command2Send:`Zynq@[123]i2c write(usbc_i2c_2,0x39,6,08,04,47,50,73,6c)`


