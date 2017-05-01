# Install Certificate:

*This utility program enables the developer to add the certificate for a particular site(url) in to the keystore file **cacerts**.* 
## Adding the SSL certificate in to the JDK home directory.

>This program gets the keystore file from the JDK home directory currently configured in the system. The *cacerts* keystore is then updated with the
certificate fetched from the specified url. The program asks the user to select the certificate to be added in the and then generates a copy of the 
cacert under the current directory where this program is being executed.

## Usage:

> Compile the program
>> `$javac InstallCert.java`

> Run from the current directory
>> `$java InstallCert <url>:<port>`

>The url and port values represents the site where the certificate has to be downloaded and added to the keystore. The port value will be 443 in most cases

## Note:
> The generated cacerts file under the current directory where the program was executed, should be copied and added to the JDK home `$JAVA_HOME\jre\lib\security`.
After this you should be able to programatically do a http request to ssl site wil out any certificate issue.
