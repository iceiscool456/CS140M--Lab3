# CS140M--Lab3

Part 3:
  1.
    The address for the accelerometer is 0011001b while the address for the magnetometer is 0011110b.
  2.
    The sub-address represents the register address inside the sensor, while the I2C address selects the sensor. 
  3.
    CTRL_REG1_A is the register address and it is at  0100000. For the lab I'll be working with 100hz, so we would configure the correct CTRL_REG1_A bits as 01010111.
  4.
    The addresses that would be used are  00101000 for OUT_X_L_A,  00101001 for OUT_X_H_A, 00101010 for OUT_Y_L_A, 00101011 for OUT_Y_H_A,  00101100 for OUT_Z_L_A, and  00101101 for OUT_Z_H_A.

Part 5:
  1. 
    Since we're utilizing only one read, we need to configure the starting sub-address to have it's MSB as 1, thus enabling auto-incrementing. From then on, we can store the values in an array and utilize them, we also need to modify the size to 6, since we need to store each axis' data, and each of those axis' have both a low and high byte. 
