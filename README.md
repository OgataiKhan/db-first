# DB First

In this project I model a table representing used cars being sold in a dealership. For each data column I specify the name, the SQL Data Type, and applicable constraints.

### ID

This is the primary key. It needs to be NOT NULL, UNIQUE, and it needs to AUTO_INCREMENT. It will be a MEDIUMINT value, which should be sufficient for the entire lifetime of operation of a typical dealership.

### Brand

The brand name is generally a single word or acronym, VARCHAR(50) allows us to type in the full name in the case of an acronym. Assuming the dealership does not deal in custom built cars for legal reasons, the field should always be NOT NULL.

### Model

Similarly, VARCHAR(50) should be able to accomodate most car model names and the field should be NOT NULL.

### Year

SMALLINT is sufficient for the year of manufacture. The field can be NULL in case the year is unknown, but in the vast majority of cases it should be specified.

### Color

VARCHAR(30) is sufficient for the vast majority of English color names, even particularly niche ones. As even an unpainted car has a color, the field should be NOT NULL. A multicolored car should be designated as "Various" or "Multicolored".

### Body Type

E.g., sedan, SUV, coupe. VARCHAR(30) is sufficient for most car body type descriptions. The field can be NULL in case it is difficult to determine the body type of an unusual car.

### Mileage

Generally cars last about 200,000 to 300,000 miles with proper maintenance, so INT is necessary to represent mileage. The field can be NULL in case the engine has been replaced and the total mileage is unknown.

### Engine Type

E.g., V6, electric, hybrid. VARCHAR(50) is sufficient for most engine types. The field should always be NOT NULL for a functioning car.

### Transmission

E.g., manual, automatic. VARCHAR(50) is used to account for, for example, Continuously Variable Transmission. The field should always be NOT NULL.

### VIN

The Vehicle Identification Number is a unique 17-character code used to identify motor vehicles. CHAR(17) is used, and the value should be NOT NULL and UNIQUE.

### License Plate Number

License plate numbers vary by country but generally do not exceed 10-12 characters, so VARCHAR(15) should be sufficient. this should also be NOT NULL and UNIQUE for legal reasons.

### Number of Previous Owners

TINYINT is more than enough to represent this. Can be NULL in case this information is unknown, defaults to 0.

### Accident History

Represented as TEXT to give room for accurate descriptions, can be NULL in case the information is unknown, defaults to 'None'.

### Service History

Represented as TEXT, can be NULL in case the information is unknown.

### Price

DECIMAL(10,2) is enough for even the most expensive cars. For a more typical dealership a smaller number of digits can be used. Prices are best represented with DECIMAl for accuracy. Can be NULL for cars not on sale, defaults to 0.

### Warranty Info, Interior Features, Exterior Features, Safety Features

All represented by TEXT and can be NULL in case of unknown information.

### Emission Standard

VARCHAR(15) is sufficient to represent most emission standards in use. Can be NULL for cars that do not respect any emission standards.

### Date of Listing

Represented as a DATE, should always be NOT NULL for organizational purposes.

### Availability

Indicates if the car is available, sold, or reserved. Could be represented by a single letter with CHAR(1), but VARCHAR(15) lets us fit the entire word for clarity. Should always be NOT NULL.