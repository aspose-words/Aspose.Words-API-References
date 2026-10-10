---
title: "XmlDsigLevel"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words для Java"
description: "Указывает уровень цифровой подписи, основанный на стандарте XML-DSig, в Java."
type: docs
weight: 747
url: /ru/java/com.aspose.words/xmldsiglevel/
---

**Inheritance:**
java.lang.Object
```
public class XmlDsigLevel
```

Указывает уровень цифровой подписи в соответствии со стандартом XML-DSig.

 **Examples:** 

Показывает, как подписать документ на основе стандарта XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [XML_D_SIG](#XML-D-SIG) | Указывает уровень подписи XML-DSig. |
| [X_AD_ES_EPES](#X-AD-ES-EPES) | Указывает уровень подписи XAdES-EPES. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String xmlDsigLevelName)](#fromName-java.lang.String) |  |
| [getName(int xmlDsigLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xmlDsigLevel)](#toString-int) |  |
### XML_D_SIG {#XML-D-SIG}
```
public static int XML_D_SIG
```


Указывает уровень подписи XML-DSig.

 **Remarks:** 

Простая цифровая подпись, которой не следует доверять после истечения срока действия её сертификата подписи.

### X_AD_ES_EPES {#X-AD-ES-EPES}
```
public static int X_AD_ES_EPES
```


Указывает уровень подписи XAdES-EPES.

 **Remarks:** 

Добавляет информацию о сертификате подписи в подпись XML-DSig. Злоумышленник не может заменить сертификат подписи другим сертификатом с тем же открытым/закрытым ключом.

### length {#length}
```
public static int length
```


### fromName(String xmlDsigLevelName) {#fromName-java.lang.String}
```
public static int fromName(String xmlDsigLevelName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlDsigLevelName | java.lang.String |  |

**Returns:**
int
### getName(int xmlDsigLevel) {#getName-int}
```
public static String getName(int xmlDsigLevel)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlDsigLevel | int |  |

**Returns:**
java.lang.String
