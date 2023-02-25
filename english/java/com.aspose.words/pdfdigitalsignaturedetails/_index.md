---
title: PdfDigitalSignatureDetails
linktitle: PdfDigitalSignatureDetails
second_title: Aspose.Words for Java API Reference
description: Contains details for signing a PDF document with a digital signature in Java.
type: docs
weight: 457
url: /java/com.aspose.words/pdfdigitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfDigitalSignatureDetails
```

Contains details for signing a PDF document with a digital signature.

At the moment digitally signing PDF documents is only available on .NET 2.0 or higher.

To digitally sign a PDF document when it is created by Aspose.Words, set the [PdfSaveOptions.getDigitalSignatureDetails()](../../com.aspose.words/pdfsaveoptions/\#getDigitalSignatureDetails) / [PdfSaveOptions.setDigitalSignatureDetails(com.aspose.words.PdfDigitalSignatureDetails)](../../com.aspose.words/pdfsaveoptions/\#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails) property to a valid [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) object and then save the document in the PDF format passing the [PdfSaveOptions](../../com.aspose.words/pdfsaveoptions/) as a parameter into the [Document.save(java.lang.String, com.aspose.words.SaveOptions)](../../com.aspose.words/document/\#save-java.lang.String--com.aspose.words.SaveOptions) method.

Aspose.Words creates a PKCS\#7 signature over the whole PDF document and uses the "Adobe.PPKMS" filter and "adbe.pkcs7.sha1" subfilter when creating a digital signature.
## Constructors

| Constructor | Description |
| --- | --- |
| [PdfDigitalSignatureDetails()](#PdfDigitalSignatureDetails) | Initializes an instance of this class. |
| [PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)](#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date) | Initializes an instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getCertificateHolder()](#getCertificateHolder) | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [getClass()](#getClass) |  |
| [getHashAlgorithm()](#getHashAlgorithm) | Gets the hash algorithm. |
| [getLocation()](#getLocation) | Gets the location of the signing. |
| [getReason()](#getReason) | Gets the reason for the signing. |
| [getSignatureDate()](#getSignatureDate) | Gets the date of the signing. |
| [getTimestampSettings()](#getTimestampSettings) | Gets the digital signature timestamp settings. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [setHashAlgorithm(int value)](#setHashAlgorithm-int) | Sets the hash algorithm. |
| [setLocation(String value)](#setLocation-java.lang.String) | Sets the location of the signing. |
| [setReason(String value)](#setReason-java.lang.String) | Sets the reason for the signing. |
| [setSignatureDate(Date value)](#setSignatureDate-java.util.Date) | Sets the date of the signing. |
| [setTimestampSettings(PdfDigitalSignatureTimestampSettings value)](#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings) | Sets the digital signature timestamp settings. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### PdfDigitalSignatureDetails() {#PdfDigitalSignatureDetails}
```
public PdfDigitalSignatureDetails()
```


Initializes an instance of this class.

### PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate) {#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date}
```
public PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)
```


Initializes an instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | A certificate holder which contains the certificate itself. |
| reason | java.lang.String | The reason for signing. |
| location | java.lang.String | The location of signing. |
| signatureDate | java.util.Date | The date and time of signing. |

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Returns the certificate holder object that contains the certificate was used to sign the document.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The certificate holder object that contains the certificate was used to sign the document.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getHashAlgorithm() {#getHashAlgorithm}
```
public int getHashAlgorithm()
```


Gets the hash algorithm. The default value is the SHA-256 algorithm.

**Returns:**
int - The hash algorithm. The returned value is one of [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/) constants.
### getLocation() {#getLocation}
```
public String getLocation()
```


Gets the location of the signing. The default value is  null .

**Returns:**
java.lang.String - The location of the signing.
### getReason() {#getReason}
```
public String getReason()
```


Gets the reason for the signing. The default value is  null .

**Returns:**
java.lang.String - The reason for the signing.
### getSignatureDate() {#getSignatureDate}
```
public Date getSignatureDate()
```


Gets the date of the signing.

The default value is the current time.

This value will appear in the digital signature as an unverified computer time.

**Returns:**
java.util.Date - The date of the signing.
### getTimestampSettings() {#getTimestampSettings}
```
public PdfDigitalSignatureTimestampSettings getTimestampSettings()
```


Gets the digital signature timestamp settings.

The default value is  null  and the digital signature will not be time-stamped. When this property is set to a valid [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) object, then the digital signature in the PDF document will be time-stamped.

**Returns:**
[PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) - The digital signature timestamp settings.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


Returns the certificate holder object that contains the certificate was used to sign the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | The certificate holder object that contains the certificate was used to sign the document. |

### setHashAlgorithm(int value) {#setHashAlgorithm-int}
```
public void setHashAlgorithm(int value)
```


Sets the hash algorithm. The default value is the SHA-256 algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The hash algorithm. The value must be one of [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/) constants. |

### setLocation(String value) {#setLocation-java.lang.String}
```
public void setLocation(String value)
```


Sets the location of the signing. The default value is  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The location of the signing. |

### setReason(String value) {#setReason-java.lang.String}
```
public void setReason(String value)
```


Sets the reason for the signing. The default value is  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The reason for the signing. |

### setSignatureDate(Date value) {#setSignatureDate-java.util.Date}
```
public void setSignatureDate(Date value)
```


Sets the date of the signing.

The default value is the current time.

This value will appear in the digital signature as an unverified computer time.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The date of the signing. |

### setTimestampSettings(PdfDigitalSignatureTimestampSettings value) {#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings}
```
public void setTimestampSettings(PdfDigitalSignatureTimestampSettings value)
```


Sets the digital signature timestamp settings.

The default value is  null  and the digital signature will not be time-stamped. When this property is set to a valid [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) object, then the digital signature in the PDF document will be time-stamped.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) | The digital signature timestamp settings. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

