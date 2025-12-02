<div align="center">

# Exodus TwinLock Bypass

## Context and Intent
In the prevailing digital landscape, the imperative of ensuring the veracity and integrity of our shared and utilized data stands paramount. Amidst the intricate tapestry of security measures, safeguarding our APIs assumes pivotal significance. Presented here is an elucidation of my approach to fortify Django REST Framework JWT through the cloak of Twilio 2FA. This unveiling aspires to alleviate the arduous process of integrating Twilio 2FA into REST APIs while upholding steadfast security. This compendium is a testament to my journey in harmonizing Django with Twilio's Authy API for Python.

![Exodus_Logo-removebg-preview](https://user-images.githubusercontent.com/106811566/171853360-e2a350e4-76f5-49f1-8962-f11034941d87.png)



<!----------------------------------------------------------------------------------------------->


<!----------------------------------------------------------------------------------------------->


## **Highlighted Attributes**

**Diverse Support for OTP Codes in Exodus Stealer:**
1. Delivery of Codes Directly to Users
2. TOTP (Google Authenticator) Codes Grounded on Shared Secret (HMAC)

**Customizable Configuration:**
- Tailored Length of OTP Code Digits
- Adaptable Threshold for Maximum Login Attempts
- Custom Logic to Discern Necessity of Two-Factor Authentication
- Configurable Window of Time Eclipsing Subsequent 2FA Requests

**Enhanced Security:**
- Potential Encryption of TOTP Secret within Database
- Encryption Augmented with IV (Initialization Vector) and Salt

## **Magento 2 Two Factor Authentication Module**
An Illustrated Glimpse into the Magento 2 Two Factor Authentication Module
![image](https://user-images.githubusercontent.com/106811566/171853515-21f66070-ca76-45c7-a38b-e67da66989f1.png)

The Momentum of Progress:
- The future harbors the envisioning of Google Authenticator safeguarding the realms of both customer and admin accounts within a Magento 2 store.
- With a dash of audacity, this project endeavors to traverse diverse aspects of Magento 2 functionality and experimentation.
- In time, as the culmination materializes, the creation shall find its residence within Packagist, rendering it available for download.
- However, as the present stage reflects an early juncture, functionality remains distant, and risk accompanies its usage.

It's advised to embark on this journey with a full understanding of its developmental state and its concomitant perils.





<!----------------------------------------------------------------------------------------------->




## **Collaborative Efforts Welcome**
We extend a warm embrace to contributions in the form of pull requests, bug reports, and any other constructive inputs. Our aspiration particularly inclines towards achieving full compatibility of this gem with Rails 5+ and rectifying any lingering deprecation messages.

## **Illustrative Application**
Within the precincts of the `demo` directory, an exemplary Rails 4 application takes center stage. This platform serves as a canvas to illustrate the operational essence of Devise-Two-Factor, allowing you to visualize its dynamics in a streamlined manner. More importantly, it functions as a compass guiding you through the integration of this gem into your own application.

To ensure the smooth functioning of the demo app, the creation of an encryption key is pivotal. This key should then be stored as an environment variable. A recommended method entails crafting a `local_env.yml` file within the root of the application. Inside this YAML file, allocate a value to `ENCRYPTION_KEY`. Upon loading, the value you designate here will permeate the application environment via `application.rb`.


<!----------------------------------------------------------------------------------------------->



## **Initiating the Journey**

The embarkation into Devise-Two-Factor's realm necessitates a few prerequisites, but the entry is a seamless one:

1. **Rails Application with Devise:** Lay the foundation with a Rails application equipped with Devise. Find guidance on how to accomplish this on the [Devise homepage](https://github.com/plataformatec/devise).


<!----------------------------------------------------------------------------------------------->



## **Current Status**

From the vantage point I hold, this project seems to have reached a state of functional completeness. A substantial number of tests have been meticulously crafted to underpin its solidity.

My heartfelt appreciation extends to Alan Storm and his [travis repository](https://github.com/astorm/magento2-travis). It facilitated the establishment of a testing framework, aiding me in shaping the testing landscape.

For now, the repository is configured for tests and has begun to embrace them.


<!----------------------------------------------------------------------------------------------->

## **Command Line Capabilities**

- Adding a New Key: `2fa -add name`
- Generating Two-Factor Key: `2fa name`
- Listing All Keys: `2fa -list`
- Generating and Copying to Clipboard: `2fa name -clip`
- Default Time-Based Authentication Codes: `2fa`

For exhaustive details on these commands and their attributes, the repository itself serves as a treasure trove of knowledge.


<!----------------------------------------------------------------------------------------------->

## **Illustrative Scenario**

In the process of setting up GitHub's Two-Factor Authentication (2FA), a pivotal juncture arrives during the "Scan this barcode with your app" phase. Amidst this step, a hyperlink beckons, marked "enter this text code instead." Upon invoking this link, a window unfurls, divulging "your two-factor secret," a succinct amalgamation of letters and digits.

The process of assimilating this secret into 2fa entails invoking the command `2fa -add github` and inputting the secret when prompted:

```bash
$ 2fa -add github
2fa key for github: nzxxiidbebvwk6jb
$
```

Upon completing this step, whenever GitHub solicits a 2FA code, the 2fa command can be summoned to fetch one:

```bash
$ 2fa github
268346
$
```

For a more succinct rendition:

```bash
$ 2fa
268346	github
$
```

While strides have been made in testing and refining, there remains a journey ahead: additional testing, refactoring, and comprehensive documentation. In the backdrop, the fortress of two-factor authentication stands resolute, securing computer systems and files with unyielding determination.

</div>

<!----------------------------------------------------------------------------------------------->