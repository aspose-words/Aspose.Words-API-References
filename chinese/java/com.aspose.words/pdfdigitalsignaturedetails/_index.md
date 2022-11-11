---
title: PdfDigitalSignatureDetails
second_title: Aspose.Words for Java API 参考
description:包含使用数字签名签署 PDF 文档的详细信息。
type: docs
weight: 451
url: /zh/java/com.aspose.words/pdfdigitalsignaturedetails/
---

**遗产:**
java.lang.Object
```
public class PdfDigitalSignatureDetails
```

包含使用数字签名签署 PDF 文档的详细信息。

目前，数字签名 PDF 文档仅适用于 .NET 2.0 或更高版本。

要在 Aspose.Words 创建 PDF 文档时对其进行数字签名，请设置[PdfSaveOptions.getDigitalSignatureDetails()](../../com.aspose.words/pdfsaveoptions\#getDigitalSignatureDetails--) / [PdfSaveOptions.setDigitalSignatureDetails(com.aspose.words.PdfDigitalSignatureDetails)](../../com.aspose.words/pdfsaveoptions\#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails-)属性为有效[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails)对象，然后将文档保存为通过[PdfSaveOptions](../../com.aspose.words/pdfsaveoptions)作为参数进入[Document.save(java.lang.String, com.aspose.words.SaveOptions)](../../com.aspose.words/document\#save-java.lang.String--com.aspose.words.SaveOptions-)方法。

Aspose.Words 创建一个 PKCS\#7 对整个 PDF 文档进行签名，并在创建数字签名时使用“Adobe.PPKMS”过滤器和“adbe.pkcs7.sha1”子过滤器。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [PdfDigitalSignatureDetails()](#PdfDigitalSignatureDetails--) | 初始化此类的一个实例。 |
| [PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)](#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date-) | 初始化此类的一个实例。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCertificateHolder()](#getCertificateHolder--) | 返回包含用于签署文档的证书的证书持有者对象。 |
| [get班级()](#get班级--) |  |
| [getHashAlgorithm()](#getHashAlgorithm--) | 获取哈希算法。 |
| [getLocation()](#getLocation--) | 获取签名的位置。 |
| [getReason()](#getReason--) | 获取签名的原因。 |
| [getSignatureDate()](#getSignatureDate--) | 获取签署日期。 |
| [getTimestampSettings()](#getTimestampSettings--) | 获取数字签名时间戳设置。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder-) | 返回包含用于签署文档的证书的证书持有者对象。 |
| [setHashAlgorithm(int value)](#setHashAlgorithm-int-) | 设置哈希算法。 |
| [setLocation(String value)](#setLocation-java.lang.String-) | 设置签名的位置。 |
| [setReason(String value)](#setReason-java.lang.String-) | 设置签名的原因。 |
| [setSignatureDate(Date value)](#setSignatureDate-java.util.Date-) | 设置签署日期。 |
| [setTimestampSettings(PdfDigitalSignatureTimestampSettings value)](#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings-) | 设置数字签名时间戳设置。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PdfDigitalSignatureDetails() {#PdfDigitalSignatureDetails--}
```
public PdfDigitalSignatureDetails()
```


初始化此类的一个实例。

### PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate) {#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date-}
```
public PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)
```


初始化此类的一个实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder) | 包含证书本身的证书持有者。 |
| reason | java.lang.String | 签约的原因。 |
| location | java.lang.String | 签约地点。 |
| signatureDate | java.util.Date | 签字的日期和时间。 |

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getCertificateHolder() {#getCertificateHolder--}
```
public CertificateHolder getCertificateHolder()
```


返回包含用于签署文档的证书的证书持有者对象。

**退货:**
[CertificateHolder](../../com.aspose.words/certificateholder) - 包含证书的证书持有者对象用于签署文档。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getHashAlgorithm() {#getHashAlgorithm--}
```
public int getHashAlgorithm()
```


获取哈希算法。默认值为 SHA-256 算法。

**退货:**
int - 哈希算法。返回值是以下之一[PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm)常数。
### getLocation() {#getLocation--}
```
public String getLocation()
```


获取签名的位置。默认值为空。

**退货:**
java.lang.String - 签名的位置。
### getReason() {#getReason--}
```
public String getReason()
```


获取签名的原因。默认值为空。

**退货:**
java.lang.String - 签名的原因。
### getSignatureDate() {#getSignatureDate--}
```
public Date getSignatureDate()
```


获取签署日期。

默认值为当前时间。

该值将作为未经验证的计算机时间出现在数字签名中。

**退货:**
java.util.Date - 签署日期。
### getTimestampSettings() {#getTimestampSettings--}
```
public PdfDigitalSignatureTimestampSettings getTimestampSettings()
```


获取数字签名时间戳设置。

默认值为空，数字签名不会加时间戳。当此属性设置为有效时[PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings)对象，则 PDF 文档中的数字签名将被加盖时间戳。

**退货:**
[PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings) - 数字签名时间戳设置。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder-}
```
public void setCertificateHolder(CertificateHolder value)
```


返回包含用于签署文档的证书的证书持有者对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder) | 包含证书的证书持有者对象用于签署文档。 |

### setHashAlgorithm(int value) {#setHashAlgorithm-int-}
```
public void setHashAlgorithm(int value)
```


设置哈希算法。默认值为 SHA-256 算法。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 哈希算法。该值必须是以下之一[PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm)常数。 |

### setLocation(String value) {#setLocation-java.lang.String-}
```
public void setLocation(String value)
```


设置签名的位置。默认值为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 签约地点。 |

### setReason(String value) {#setReason-java.lang.String-}
```
public void setReason(String value)
```


设置签名的原因。默认值为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 签约的原因。 |

### setSignatureDate(Date value) {#setSignatureDate-java.util.Date-}
```
public void setSignatureDate(Date value)
```


设置签署日期。

默认值为当前时间。

该值将作为未经验证的计算机时间出现在数字签名中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date | 签署日期。 |

### setTimestampSettings(PdfDigitalSignatureTimestampSettings value) {#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings-}
```
public void setTimestampSettings(PdfDigitalSignatureTimestampSettings value)
```


设置数字签名时间戳设置。

默认值为空，数字签名不会加时间戳。当此属性设置为有效时[PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings)对象，则 PDF 文档中的数字签名将被加盖时间戳。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings) | 数字签名时间戳设置。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
