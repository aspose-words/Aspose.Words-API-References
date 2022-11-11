---
title: SignOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify options for document signing.
type: docs
weight: 523
url: /java/com.aspose.words/signoptions/
---

**Inheritance:**
java.lang.Object
```
public class SignOptions
```

Allows to specify options for document signing.

To learn more, visit the **Work with Digital Signatures** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getComments()](#getComments--) | Specifies comments on the digital signature. |
| [getDecryptionPassword()](#getDecryptionPassword--) | The password to decrypt source document. |
| [getProviderId()](#getProviderId--) | Specifies the class ID of the signature provider. |
| [getSignTime()](#getSignTime--) | The date of signing. |
| [getSignatureLineId()](#getSignatureLineId--) | Signature line identifier. |
| [getSignatureLineImage()](#getSignatureLineImage--) | The image that will be shown in associated [SignatureLine](../../com.aspose.words/signatureline). |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setComments(String value)](#setComments-java.lang.String-) | Specifies comments on the digital signature. |
| [setDecryptionPassword(String value)](#setDecryptionPassword-java.lang.String-) | The password to decrypt source document. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID-) | Specifies the class ID of the signature provider. |
| [setSignTime(Date value)](#setSignTime-java.util.Date-) | The date of signing. |
| [setSignatureLineId(UUID value)](#setSignatureLineId-java.util.UUID-) | Signature line identifier. |
| [setSignatureLineImage(byte[] value)](#setSignatureLineImage-byte---) | The image that will be shown in associated [SignatureLine](../../com.aspose.words/signatureline). |
| [toString()](#toString--) |  |
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


Specifies comments on the digital signature. Default value is **empty string**.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getDecryptionPassword() {#getDecryptionPassword--}
```
public String getDecryptionPassword()
```


The password to decrypt source document. Default value is **empty string**. If OOXML document is encrypted, you should provide decryption password to decrypt source document before it will be signed. This is not required for documents in binary DOC format.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getProviderId() {#getProviderId--}
```
public UUID getProviderId()
```


Specifies the class ID of the signature provider. Default value is **Empty (all zeroes) Guid**.

The cryptographic service provider (CSP) is an independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption. MS Office reserves the value of \{00000000-0000-0000-0000-000000000000\} for its default signature provider.

The GUID of the additionally installed provider should be obtained from the documentation shipped with the provider.

In addition, all the installed cryptographic providers are enumerated in windows registry. It can be found in the following path: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. There is a key name "CP Service UUID" which corresponds to a GUID of signature provider.

**Returns:**
java.util.UUID - The corresponding java.util.UUID value.
### getSignTime() {#getSignTime--}
```
public Date getSignTime()
```


The date of signing. Default value is **current time**.

**Returns:**
java.util.Date - The corresponding java.util.Date value.
### getSignatureLineId() {#getSignatureLineId--}
```
public UUID getSignatureLineId()
```


Signature line identifier. Default value is **Empty (all zeroes) Guid**. When set, it associates [SignatureLine](../../com.aspose.words/signatureline) with corresponding [DigitalSignature](../../com.aspose.words/digitalsignature).

**Returns:**
java.util.UUID - The corresponding java.util.UUID value.
### getSignatureLineImage() {#getSignatureLineImage--}
```
public byte[] getSignatureLineImage()
```


The image that will be shown in associated [SignatureLine](../../com.aspose.words/signatureline). Default value is  null .

**Returns:**
byte[] - The corresponding byte[] value.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setComments(String value) {#setComments-java.lang.String-}
```
public void setComments(String value)
```


Specifies comments on the digital signature. Default value is **empty string**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setDecryptionPassword(String value) {#setDecryptionPassword-java.lang.String-}
```
public void setDecryptionPassword(String value)
```


The password to decrypt source document. Default value is **empty string**. If OOXML document is encrypted, you should provide decryption password to decrypt source document before it will be signed. This is not required for documents in binary DOC format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID-}
```
public void setProviderId(UUID value)
```


Specifies the class ID of the signature provider. Default value is **Empty (all zeroes) Guid**.

The cryptographic service provider (CSP) is an independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption. MS Office reserves the value of \{00000000-0000-0000-0000-000000000000\} for its default signature provider.

The GUID of the additionally installed provider should be obtained from the documentation shipped with the provider.

In addition, all the installed cryptographic providers are enumerated in windows registry. It can be found in the following path: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. There is a key name "CP Service UUID" which corresponds to a GUID of signature provider.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.UUID | The corresponding java.util.UUID value. |

### setSignTime(Date value) {#setSignTime-java.util.Date-}
```
public void setSignTime(Date value)
```


The date of signing. Default value is **current time**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The corresponding java.util.Date value. |

### setSignatureLineId(UUID value) {#setSignatureLineId-java.util.UUID-}
```
public void setSignatureLineId(UUID value)
```


Signature line identifier. Default value is **Empty (all zeroes) Guid**. When set, it associates [SignatureLine](../../com.aspose.words/signatureline) with corresponding [DigitalSignature](../../com.aspose.words/digitalsignature).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.UUID | The corresponding java.util.UUID value. |

### setSignatureLineImage(byte[] value) {#setSignatureLineImage-byte---}
```
public void setSignatureLineImage(byte[] value)
```


The image that will be shown in associated [SignatureLine](../../com.aspose.words/signatureline). Default value is  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte[] | The corresponding byte[] value. |

### toString() {#toString--}
```
public String toString()
```




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

