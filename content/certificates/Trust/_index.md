+++
description = 'Why trust matters in Cyber Security'
title = 'Trust'
weight = 3
+++

What is a certificates?

Imagine you get pulled over by police or you want to get access into an exclusive club.

You maybe asked to show your ID Card or Driver's License? How do they know it's not fake or a counterfit? They VERIFY!

Similar to how digital certificates work for computers.

If we go back to using a driver license as an example, it'll have multiple attributes to help identify you.

[*] Your Name
[*] Your Photo (Visual image of your identity, so it can be verified)
[*] Exipration Date (Valid until 2030)
[*] Issuer (DLVA/DMV)

A digital certificate has similar attributes.

[*] Subject: The name of the Website (eg. barclays.co.uk)
[*] Valid Dates: Start and end dates the certificate is valid between
[*] Issuer: Who has signed to verify the identity of the subject.

Why do we need Certificates?

If you want to visit your bank website, you'll type in the URL of the bank. As soon as you type in the URL (www.barclays.co.uk).

How do you know you are visiting the correct website and not someone incept and capture your login information? You need to verify the certificate present with a independent authoritiy, who are called certificate authorities. These can be seen as DLVA/DMV, as they are responsible for issuing digital certificates for your request domains.

    Your browser has a list of know certificate authorities (CAs) these are globally trusted companies that meet the industry standards set by the CA/Browser Forum (https://cabforum.org/).

    As well as abiding by the industry standards said by the CA/Browser Forum. It's required that security is held to the highest levels from regular independant strict audits and secure infrastructure with the use of offline hardware security modules (HSMs) along side your physical security. 

You visit the bank website and get presented a certificate, you're browser then validates that the Subject mataches the URL for the certificate as well as ensuring the dates are correct. 

    Your browser will also query the certificate for something we've not mentioned yet which are CRLs (Certificate Revoke List) or by OCSP (Online Certificate Status Protocol).

    If a certificate is unable to reach the CRL or OCSP, the certificate will be deemed invalid and unstrusted depending on the settings of the client. These settings can be overridden if you ever see the "Skip Certificate Verification" option. (Not Recommended)

If the certificate has passed the different checks mentioned preiosuly and been verified by a trusted certificate authority (CA), it'll establish a TLS connection and complete a key exchange.

[*] Does the URL typed in the Browser match the certificate Subject name or Subject Alternative Name (SANs)
[*] Date is valid and between start and end dates.
[*] Check Issuer is CA trusted
[*] Certificate isn't on a revoke list (CRLs or OCSP)

