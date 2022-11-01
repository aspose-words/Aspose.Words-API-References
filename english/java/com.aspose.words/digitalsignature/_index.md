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
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCertificateHolder()](#getCertificateHolder--) | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [getClass()](#getClass--) |  |
| [getComments()](#getComments--) | Gets the signing purpose comment. |
| [getIssuerName()](#getIssuerName--) | Returns the subject distinguished name of the certificate isuuer. |
| [getSignTime()](#getSignTime--) | Gets the time the document was signed. |
| [getSignatureType()](#getSignatureType--) | Gets the type of the digital signature. |
| [getSubjectName()](#getSubjectName--) | Returns the subject distinguished name of the certificate that was used to sign the document. |
| [hashCode()](#hashCode--) |  |
| [isValid()](#isValid--) | Returns true if this digital signature is valid and the document has not been tampered with. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) | Returns a user-friendly string that displays the value of this object. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getCertificateHolder() {#getCertificateHolder--}
```
public CertificateHolder getCertificateHolder()
```


Returns the certificate holder object that contains the certificate was used to sign the document.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder) - The certificate holder object that contains the certificate was used to sign the document.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getComments() {#getComments--}
```
public String getComments()
```


Gets the signing purpose comment.

**Returns:**
java.lang.String - The signing purpose comment.
### getIssuerName() {#getIssuerName--}
```
public String getIssuerName()
```


Returns the subject distinguished name of the certificate isuuer.

**Returns:**
java.lang.String - The subject distinguished name of the certificate isuuer.
### getSignTime() {#getSignTime--}
```
public Date getSignTime()
```


Gets the time the document was signed.

**Returns:**
java.util.Date - The time the document was signed.
### getSignatureType() {#getSignatureType--}
```
public int getSignatureType()
```


Gets the type of the digital signature.

**Returns:**
int - The type of the digital signature. The returned value is one of [DigitalSignatureType](../../com.aspose.words/digitalsignaturetype) constants.
### getSubjectName() {#getSubjectName--}
```
public String getSubjectName()
```


Returns the subject distinguished name of the certificate that was used to sign the document.

**Returns:**
java.lang.String - The subject distinguished name of the certificate that was used to sign the document.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isValid() {#isValid--}
```
public boolean isValid()
```


Returns true if this digital signature is valid and the document has not been tampered with.

**Returns:**
boolean - True if this digital signature is valid and the document has not been tampered with.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```


Returns a user-friendly string that displays the value of this object.

**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

