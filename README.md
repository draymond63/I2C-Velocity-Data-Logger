# I2C-Velocity-Data-Logger
A circuit logs data onto an EEPROM chip. This data is then presented on the serial plotter, using an RTC to time stamp each byte of data.

## Theory
To calculate the velocity of the hand, first the coordinates of it are measured. These values are then subtracted from its previously measured coordinates to figured out the total distance travelled over a given period. From these two lengths, x and y, Pythagorean theorem is used to calculate the total distance the object travelled. This distance value is divided by the period and then logged onto an external I2C EEPROM chip. EEPROM chips have what is essentially an array of bytes, that can be read and written to. To measure the period in j distance recordings, an RTC is used. The RTC has a square wave, which emits a 1Hz, 4KHz, 8kHz, or 32KHz waves. This allow frequency allows us to determine how often we sample from our sensors. 
