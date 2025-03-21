Place an INA219 for monitoring the battery on the I2C Bus and configure it correctly with respect to the hardware (cannot have BOTH A0 AND A1 on GND)

---

TODO

| Pin No | Name        | Purpose                                                      |
| ------ | ----------- | ------------------------------------------------------------ |
| 9      | `USART2_RX` | ? not sure if relevant                                       |
| 12     | `USART2_TX` | ? not sure if relevant                                       |
| 16     | `I2C1_SCL`  | I2C communication with current/voltage/power monitor (clock) |
| 17     | `I2C1_SDA`  | I2C communication with current/voltage/power monitor (data)  |


