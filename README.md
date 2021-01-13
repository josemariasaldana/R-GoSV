# R-GoSV

## AES256_gcm_rgoose

`AES256_gcm_rgoose.c` encrypts the GOOSE APDU data which is defined according to IEC 61850-8-2 using AES256-GCM encryption algorithm with 256 bit symmetric key and generates cipher text. The program  makes use of `openssl/hmac.h` and `openssl/evp.h` libraries.

Commands to execute the program at terminal:

Install openssl library if not installed using the following command:
```
$ sudo apt-get install libssl-dev
```

Compilation of program:
```
$ gcc -o AES256_gcm_rgoose AES256_gcm_rgoose.c -L/usr/local/lib/ -lssl -lcrypto 
```

To run the code:
```
$./AES256_gcm_rgoose
```

## HMAC_SHA256_rgoose
`HMAC_SHA256_rgoose.c` generates a digital signature for the GOOSE APDU data which is defined according to IEC 61850-8-2 using HMAC-SHA256 digital signature algorithm with 256 bit symmetric key. The program  make use of `openssl/hmac.h` and `openssl/evp.h` libraries.

Commands to execute the program at terminal:

Install openssl library if not installed using the following command:
```
$ sudo apt-get install libssl-dev
```

Compilation of program:
```
$ gcc -o HMAC_SHA256_rgoose HMAC_SHA256_rgoose.c -L/usr/local/lib/ -lssl -lcrypto 
```

To run the code:
```
$./HMAC_SHA256_rgoose
```

## R-GoSV_rgoose_send

`R-GoSV_rgoose_send.c` makes use of network interface libraries to send full stack of GOOSE APDU message which constructed according to IEC 61850-90-5 by adding IP, UDP, Session layer headers and application data. Here application data is GOOSE message defined by IEC 61850-8-1. Session layer includes all the necessary security fields. Encrypted data of session layer information along with generated digital signature is send into the network. 

Commands to execute the program at terminal:

Compilation of program:
```
$ gcc -o R-GoSV_rgoose_send R-GoSV_rgoose_send.c
```

To run the program:
(sudo allows users to run programs with the security privileges of another user, normally the superuser, or root).
```
$ sudo ./R-GoSV_rgoose_send
```

## AES256_gcm_rsv

`AES256_gcm_rsv.c` encrypts the Sample Value (SV) APDU data which is defined according to IEC 61850-9-1 using AES256-GCM encryption algorithm with 256 bit symmetric key and generates cipher text. The program  makes use of `openssl/hmac.h` and `openssl/evp.h` libraries.

Commands to execute the program at terminal:

Install openssl library if not installed using the following command. 
```
$ sudo apt-get install libssl-dev
```

Compilation of program:
```
$ gcc -o AES256_gcm_rsv AES256_gcm_rsv.c -L/usr/local/lib/ -lssl -lcrypto 
```

To run the code:
```
$./AES256_gcm_rsv
```

## HMAC_SHA256_rsv

`HMAC_SHA256_rsv.c` generates digital signature for the Sample Value (SV) APDU data which is defined according to IEC 61850-9-2 using HMAC-SHA256 digital signature algorithm with 256 bit symmetric key. The program  make use of `openssl/hmac.h` and `openssl/evp.h` libraries.

Commands to execute the program at terminal:

Install openssl library if not installed using the following command. 
```
$ sudo apt-get install libssl-dev
```

Compilation of program:
```
$ gcc -o HMAC_SHA256_rsv HMAC_SHA256_rsv.c -L/usr/local/lib/ -lssl -lcrypto 
```

To run the code:
```
$./HMAC_SHA256_rsv
```

## R-GoSV_rsv_send

`R-GoSV_rsv_send.c` makes use of network interface libraries to send full stack of Sample Value (SV) APDU message which constructed according to IEC 61850-90-5 by adding IP, UDP, Session layer headers and application data. Here application data is Sample Value (SV) APDU message defined by IEC 61850-9-2. Session layer includes all the necessary security fields. Encrypted data of session layer information along with generated digital signature is send into the network. 

Commands to execute the program at terminal:

sudo allows users to run programs with the security privileges of another user (normally the superuser, or root). 
```
$ sudo bash 
```

Compilation of program:
```
$ gcc -o R-GoSV_rsv_send R-GoSV_rsv_send.c
```

To run the program:
```
$./  R-GoSV_rsv_send
```

## plain_rgoose

`plain_rgoose.c` generates R-GOOSE packets with out any security algorithm applied to the packets and send in to the network with its full stack of all the headers of IP, UDP, Session layers followed by Application data. Here applicatio data is GOOSE message defined according to IEC 61850-8-1. 

Commands to execute the program at terminal:

Compilation of program:
```
$ gcc -o plain_rgoose plain_rgoose.c
```

To run the program:
(sudo allows users to run programs with the security privileges of another user, normally the superuser, or root).
```
$ sudo ./plain_rgoose
```

## plain_rsv
`plain_rsv.c` generates R-SV packets with out any security algorith applied to the packets and send in to the network with its full stack of all the headers of IP, UDP, Session layers followed by Application data. Here applicatio data is GOOSE message defined according to IEC 61850-8-1. 

Commands to execute the program at terminal:

Compilation of program:
```
$ gcc -o plain_rsv.c plain_rsv.c.c
```

To run the program:
(sudo allows users to run programs with the security privileges of another user, normally the superuser, or root).
```
$./plain_rsv
```
