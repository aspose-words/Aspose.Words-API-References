---
title: "XmlDsigLevel"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words for Java"
description: "指定基于 XML-DSig 标准的数字签名级别（在 Java 中）。"
type: docs
weight: 747
url: /zh/java/com.aspose.words/xmldsiglevel/
---

**Inheritance:**
java.lang.Object
```
public class XmlDsigLevel
```

指定基于 XML-DSig 标准的数字签名级别。

 **Examples:** 

展示如何基于 XML-DSig 标准对文档进行签名。

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | 指定 XML-DSig 签名级别。 |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | 指定 XAdES-EPES 签名级别。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String xmlDsigLevelName)](#fromName-java.lang.String) |  |
| [getName(int xmlDsigLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xmlDsigLevel)](#toString-int) |  |
### XML_D_SIG {#XML-D-SIG}
```
public static int XML_D_SIG
```


指定 XML-DSig 签名级别。

 **Remarks:** 

一种简单的数字签名，在其签名证书过期后不应被信任。

### X_AD_ES_EPES {#X-AD-ES-EPES}
```
public static int X_AD_ES_EPES
```


指定 XAdES-EPES 签名级别。

 **Remarks:** 

向 XML-DSig 签名添加签名证书信息。恶意用户无法使用相同公私钥的其他证书来替换签名证书。

### length {#length}
```
public static int length
```


### fromName(String xmlDsigLevelName) {#fromName-java.lang.String}
```
public static int fromName(String xmlDsigLevelName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| xmlDsigLevelName | java.lang.String |  |

**Returns:**
int
### getName(int xmlDsigLevel) {#getName-int}
```
public static String getName(int xmlDsigLevel)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xmlDsigLevel) {#toString-int}
```
public static String toString(int xmlDsigLevel)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
