# Setup

## Getting Started

In order to complete some of the challenges in SecurityShepherd, it is necessary to intercept the request between your browser and the server. To do this, use a proxy tool. Two useful ones that I have used are BurpSuite and OWASP Zed Attack Proxy.


## Install your proxy application
Download and install a proxy application that allows you to perform man-in-the-middle interceptions of requests.
Examples
 * BurpSuite (Free version is fine)
 * OWASP Zed Attack Proxy.  

## Configure your proxy application

### Burpsuite

[burpsuite1]: https://github.com/chrismcneill/securityshepherd-walkthrough/raw/master/common/images/burpsuite1.png "Burpsuite Setup Screenshot"
[burpsuite2]: https://github.com/chrismcneill/securityshepherd-walkthrough/raw/master/common/images/burpsuite2.png "Burpsuite Setup Screenshot"
[burpsuite3]: https://github.com/chrismcneill/securityshepherd-walkthrough/raw/master/common/images/burpsuite3.png "Burpsuite Setup Screenshot"
[burpsuite4]: https://github.com/chrismcneill/securityshepherd-walkthrough/raw/master/common/images/burpsuite4.png "Burpsuite Setup Screenshot"

1. Open Burpsuite (This should be achievable by double-clicking on the .jar, however some people may need to use the command prompt and run java -jar <burpsuiteFileName>.jar within the directory that burpsuite was downloaded to), and go to the "Proxy" tab, then select the "Options" tab.
![burpsuite proxy options][burpsuite1]
2. Select the first entry in the "Proxy Listeners" section and click "Edit"
Complete the dialog with the settings below:
3. Click OK on this dialog to save your settings and close the dialog.
Navigate back to the "Intercept" tab and click the "Intercept is on" button so it will now read "Intercept is off" for now.
![burpsuite listen port][burpsuite2]
![burpsuite redirect location][burpsuite3]
![burpsuite certificate selection][burpsuite4]
4. Click OK on this dialog to save your settings and close the dialog.
5. Navigate back to the "Intercept" tab and click the "Intercept is on" button so it will now read "Intercept is off" for now.

## Configure your browser to send traffic through your proxy 

It is easier to intercept the traffic using Mozilla Firefox because it allows you to configure its network traffic to go through a proxy without changing the underlying system network proxy settings (unlike Chrome and IE). This means you can intercept your firefox traffic (where you will use Security Shepherd) but not effect all your other network traffic (Skype, email, etc).

### Firefox

[firefox1]: https://github.com/chrismcneill/securityshepherd-walkthrough/raw/master/common/images/firefox1.png "Firefox Proxy Setup Screenshot"
[firefox2]: https://github.com/chrismcneill/securityshepherd-walkthrough/raw/master/common/images/firefox2.png "Firefox Proxy Setup Screenshot"
[firefox3]: https://github.com/chrismcneill/securityshepherd-walkthrough/raw/master/common/images/firefox3.png "Firefox Proxy Setup Screenshot"

1. Open the firefix menu, and select "Options"
    ![Firefox Options][firefox1]
2. Select "Advanced" and then "Network"
    ![Firefox Network Settings][firefox2]
3. Click on "Settings..." within the "Connection" section of this page
4. Enter the following details into the opened "Connection Settings" dialog
    ![Firefox Proxy Options][firefox3]
5. Click OK, and then close the "Options" tab.
6. Now all your traffic should be be redirected through port 8888 (which your proxy is listening on)
7. Navigate to Security Shepherd and use it as normal (you may need to accept a security certificate warning)





