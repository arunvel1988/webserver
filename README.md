# Apache HTTP Server  



Note: The website is purely for demonstration purpose and note suitable for production use.

#
### Update DNS record



If successful, an output similar to the following is expected:

    Saving debug log to /var/log/letsencrypt/letsencrypt.log
    No names were found in your configuration files. Please enter in your domain
    name(s) (comma and/or space separated)  (Enter 'c' to cancel):demo-apache.chriswang.tech
    Starting new HTTPS connection (1): acme-v01.api.letsencrypt.org
    Obtaining a new certificate
    Performing the following challenges:
    tls-sni-01 challenge for demo-apache.chriswang.tech
    Enabled Apache socache_shmcb module
    Enabled Apache ssl module
    Waiting for verification...
    Cleaning up challenges
    Generating key (2048 bits): /etc/letsencrypt/keys/0000_key-certbot.pem
    Creating CSR: /etc/letsencrypt/csr/0000_csr-certbot.pem
    Created an SSL vhost at /etc/apache2/sites-available/000-default-le-ssl.conf
    Enabled Apache socache_shmcb module
    Enabled Apache ssl module
    Deploying Certificate to VirtualHost /etc/apache2/sites-available/000-default-le-ssl.conf
    Enabling available site: /etc/apache2/sites-available/000-default-le-ssl.conf
    
    Please choose whether HTTPS access is required or optional.
    -------------------------------------------------------------------------------
    1: Easy - Allow both HTTP and HTTPS access to these sites
    2: Secure - Make all requests redirect to secure HTTPS access
    -------------------------------------------------------------------------------
    
    Select the appropriate number [1-2] then [enter] (press 'c' to cancel): 2
    Enabled Apache rewrite module
    Redirecting vhost in /etc/apache2/sites-available/000-default.conf to ssl vhost in /etc/apache2/sites-available/000-default-le-ssl.conf
    
    -------------------------------------------------------------------------------
    Congratulations! You have successfully enabled
    https://demo-apache.chriswang.tech
    
    You should test your configuration at:
    https://www.ssllabs.com/ssltest/analyze.html?d=demo-apache.chriswang.tech
    -------------------------------------------------------------------------------
    
    IMPORTANT NOTES:
     - Congratulations! Your certificate and chain have been saved at
       /etc/letsencrypt/live/demo-apache.chriswang.tech/fullchain.pem.
       Your cert will expire on 2017-07-25. To obtain a new or tweaked
       version of this certificate in the future, simply run certbot again
       with the "certonly" option. To non-interactively renew *all* of
       your certificates, run "certbot renew"
     - If you like Certbot, please consider supporting our work by:
    
       Donating to ISRG / Let's Encrypt:   https://letsencrypt.org/donate
       Donating to EFF:                    https://eff.org/donate-le

### Qualys SSL Report

To verify that the the HTTPS/TLS service is configured correctly, the [Qualys SSL Server Test](https://www.ssllabs.com/ssltest/analyze.html?d=demo-apache.chriswang.tech) is run. 

The test report is shown below with a big green **A**. It means the HTTPS/TLS is working as expected! 😀

![](images/ssl_report.png)

## References

### Apache Web Server
*  Basic Setup: https://www.digitalocean.com/community/tutorials/how-to-configure-the-apache-web-server-on-an-ubuntu-or-debian-vps
*  Get Started Guide: 
   http://httpd.apache.org/docs/2.4/getting-started.html

### Let's Encrypt and Certbot
* Get started: https://certbot.eff.org/#ubuntuxenial-apache

