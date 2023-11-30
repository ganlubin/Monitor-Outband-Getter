busctl |grep Sensor|sed -e 's| .*||' 

xyz.openbmc_project.ADCSensor 
xyz.openbmc_project.CurrSensor 
xyz.openbmc_project.ExitAirTempSensor 
xyz.openbmc_project.FanSensor 
xyz.openbmc_project.HwmonTempSensor 
xyz.openbmc_project.IntrusionSensor 
xyz.openbmc_project.MCUTempSensor 
xyz.openbmc_project.NVMeSensor 
xyz.openbmc_project.PSUSensor 
xyz.openbmc_project.Sensor.Record.Monitor



busctl tree xyz.openbmc_project.ADCSensor 

if type ---
busctl introspect xyz.openbmc_project.ADCSensor  /xyz/openbmc_project/sensors/voltage/P12VA
---

root@loongson-obmc:~# busctl introspect xyz.openbmc_project.ADCSensor  /xyz/openbmc_project/sensors/voltage/P12VA
NAME                                                  TYPE      SIGNATURE RESULT/VALUE                             FLAGS
org.freedesktop.DBus.Introspectable                   interface -         -                                        -
.Introspect                                           method    -         s                                        -
org.freedesktop.DBus.Peer                             interface -         -                                        -
.GetMachineId                                         method    -         s                                        -
.Ping                                                 method    -         -                                        -
org.freedesktop.DBus.Properties                       interface -         -                                        -
.Get                                                  method    ss        v                                        -
.GetAll                                               method    s         a{sv}                                    -
.Set                                                  method    ssv       -                                        -
.PropertiesChanged                                    signal    sa{sv}as  -                                        -
xyz.openbmc_project.Association.Definitions           interface -         -                                        -
.Associations                                         property  a(sss)    1 "chassis" "all_sensors" "/xyz/openb... emits-change
xyz.openbmc_project.Sensor.Threshold.Critical         interface -         -                                        -
.CriticalAlarmHigh                                    property  b         false                                    emits-change
.CriticalAlarmLow                                     property  b         false                                    emits-change
.CriticalHigh                                         property  d         14.4                                     emits-change writable
.CriticalLow                                          property  d         9.6                                      emits-change writable
xyz.openbmc_project.Sensor.Threshold.Warning          interface -         -                                        -
.WarningAlarmHigh                                     property  b         false                                    emits-change
.WarningAlarmLow                                      property  b         false                                    emits-change
.WarningHigh                                          property  d         13.2                                     emits-change writable
.WarningLow                                           property  d         10.8                                     emits-change writable
xyz.openbmc_project.Sensor.Value                      interface -         -                                        -
.MaxValue                                             property  d         20                                       emits-change
.MinValue                                             property  d         0                                        emits-change
.Value                                                property  d         11.1328                                  emits-change writable
xyz.openbmc_project.State.Decorator.Availability      interface -         -                                        -
.Available                                            property  b         true                                     emits-change writable
xyz.openbmc_project.State.Decorator.OperationalStatus interface -         -                                        -
.Functional                                           property  b         true                                     emits-change




