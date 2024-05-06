# MODBUS-READ-HOLDING-REGISTERS-RFID-AS-SLAVE
![image](https://github.com/VanHuyTran24/MODBUS-READ-HOLDING-REGISTERS-RFID-AS-SLAVE/assets/166670555/3c77b700-5407-4d49-8ae8-94be78cc041d)

Reads the binary contents of holding registers (4x reference) in the RFID.

A request to read registers starting at 40030 to 0000H, 00001H, …., and 0009H (ID is in registers 40032 and 40033), in slave device 1:
## Request frame of Master (Laptop)
01 03 00 00 00 05 84 4D

| Field Name                          | Value (Hex) |
| ----------------------------------- | ------------| 
| Slave Address                       | 01          |
| Function                            | 03          |
| Starting Address Hi                 | 00          |
| Starting Address Lo                 | 1E          |
| Number of Points (registers) Hi     | 00          |
| Number of Points (registers) Lo     | 05          |
| CRC Hi                              | E5          |
| CRC Lo                              | CF          |

## Response frame of Slave (RFID)
| Field Name                          | Value (Hex) |
| ----------------------------------- | ------------| 
| Slave Address                       | 01          |
| Function                            | 03          |
| Byte count                          | 00          |
| Data Hi                             | 1E          |
| Data Lo                             | 00          |
| Data Hi                             | 1E          |
| Data Lo                             | 00          |
| Data Hi (ID)                        | 1E          |
| Data Lo (ID)                        | 00          |
| Data Hi (ID)                        | 1E          |
| Data Lo (ID)                        | 00          |
| Data Hi                             | 1E          |
| Data Lo                             | 00          |
| CRC Hi                              | 1E          |
| CRC Lo                              | 00          |

 
