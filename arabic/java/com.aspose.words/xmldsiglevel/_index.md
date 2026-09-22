---
title: "XmlDsigLevel"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words لـ Java"
description: "يحدد مستوى التوقيع الرقمي بناءً على معيار XML-DSig في Java."
type: docs
weight: 747
url: /ar/java/com.aspose.words/xmldsiglevel/
---

**Inheritance:**
java.lang.Object
```
public class XmlDsigLevel
```

يحدد مستوى التوقيع الرقمي بناءً على معيار XML-DSig.

 **Examples:** 

يعرض كيفية توقيع مستند بناءً على معيار XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | يحدد مستوى توقيع XML-DSig. |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | يحدد مستوى توقيع XAdES-EPES. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String xmlDsigLevelName)](#fromName-java.lang.String) |  |
| [getName(int xmlDsigLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xmlDsigLevel)](#toString-int) |  |
### XML_D_SIG {#XML-D-SIG}
```
public static int XML_D_SIG
```


يحدد مستوى توقيع XML-DSig.

 **Remarks:** 

توقيع رقمي بسيط لا ينبغي الوثوق به بعد انتهاء صلاحية شهادة التوقيع الخاصة به.

### X_AD_ES_EPES {#X-AD-ES-EPES}
```
public static int X_AD_ES_EPES
```


يحدد مستوى توقيع XAdES-EPES.

 **Remarks:** 

يضيف معلومات حول شهادة التوقيع إلى توقيع XML-DSig. لا يمكن للمستخدم الخبيث استبدال شهادة التوقيع بشهادة أخرى لها نفس المفتاح العام/الخاص.

### length {#length}
```
public static int length
```


### fromName(String xmlDsigLevelName) {#fromName-java.lang.String}
```
public static int fromName(String xmlDsigLevelName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlDsigLevelName | java.lang.String |  |

**Returns:**
int
### getName(int xmlDsigLevel) {#getName-int}
```
public static String getName(int xmlDsigLevel)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
