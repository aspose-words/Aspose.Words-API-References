---
title: DigitalSignature
second_title: Aspose.Words for Java API Reference
description: Represents a digital signature on a document and the result of its verification.
type: docs
weight: 111
url: /java/com.aspose.words/digitalsignature/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignature
```

Represents a digital signature on a document and the result of its verification.

To learn more, visit the **Work with Digital Signatures** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSignatureType()](#getSignatureType--) | Gets the type of the digital signature. |
| [getSignTime()](#getSignTime--) | Gets the time the document was signed. |
| [getComments()](#getComments--) | Gets the signing purpose comment. |
| [getSubjectName()](#getSubjectName--) | Returns the subject distinguished name of the certificate that was used to sign the document. |
| [getIssuerName()](#getIssuerName--) | Returns the subject distinguished name of the certificate isuuer. |
| [isValid()](#isValid--) | Returns true if this digital signature is valid and the document has not been tampered with. |
| [getCertificateHolder()](#getCertificateHolder--) | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [toString()](#toString--) | Returns a user-friendly string that displays the value of this object. |
### getSignatureType() {#getSignatureType--}
```
public int getSignatureType()
```


Gets the type of the digital signature.

**Returns:**
int - The type of the digital signature. The returned value is one of [DigitalSignatureType](../../com.aspose.words/digitalsignaturetype) constants.
### getSignTime() {#getSignTime--}
```
public Date getSignTime()
```


Gets the time the document was signed.

**Returns:**
java.util.Date - The time the document was signed.
### getComments() {#getComments--}
```
public String getComments()
```


Gets the signing purpose comment.

**Returns:**
java.lang.String - The signing purpose comment.
### getSubjectName() {#getSubjectName--}
```
public String getSubjectName()
```


Returns the subject distinguished name of the certificate that was used to sign the document.

**Returns:**
java.lang.String - The subject distinguished name of the certificate that was used to sign the document.
### getIssuerName() {#getIssuerName--}
```
public String getIssuerName()
```


Returns the subject distinguished name of the certificate isuuer.

**Returns:**
java.lang.String - The subject distinguished name of the certificate isuuer.
### isValid() {#isValid--}
```
public boolean isValid()
```


Returns true if this digital signature is valid and the document has not been tampered with.

**Returns:**
boolean - True if this digital signature is valid and the document has not been tampered with.
### getCertificateHolder() {#getCertificateHolder--}
```
public CertificateHolder getCertificateHolder()
```


Returns the certificate holder object that contains the certificate was used to sign the document.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder) - The certificate holder object that contains the certificate was used to sign the document.
### toString() {#toString--}
```
public String toString()
```


Returns a user-friendly string that displays the value of this object.

**Returns:**
java.lang.String
