---
title: "ContentDisposition"
linktitle: "ContentDisposition"
second_title: "Aspose.Words Java için"
description: "Java'da belgeyi istemci tarayıcısında sunmanın farklı yollarını listeler."
type: docs
weight: 126
url: /tr/java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

Belgenin istemci tarayıcısında sunulmasının farklı yollarını sıralar.

 **Remarks:** 

Gerçek tarayıcı davranışının, tarayıcının güvenlik yapılandırması tarafından etkilenebileceğini unutmayın.

 **Examples:** 

Bir posta birleştirme işleminin nasıl yapılacağını ve ardından belgenin istemci tarayıcısına kaydedileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" MERGEFIELD FullName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Company ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD City ");

 doc.getMailMerge().execute(new String[]{"FullName", "Company", "Address", "City"},
         new Object[]{"James Bond", "MI5 Headquarters", "Milbank", "London"});
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Belgeyi tarayıcıya gönderir ve belgeyi diske kaydetme ya da belgenin uzantısıyla ilişkili uygulamada açma seçeneği sunar. |
| [INLINE](#INLINE) | Belgeyi tarayıcıya gönderir ve belgeyi diske kaydetme ya da tarayıcı içinde açma seçeneği sunar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String contentDispositionName)](#fromName-java.lang.String) |  |
| [getName(int contentDisposition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int contentDisposition)](#toString-int) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


Belgeyi tarayıcıya gönderir ve belgeyi diske kaydetme ya da belgenin uzantısıyla ilişkili uygulamada açma seçeneği sunar.

### INLINE {#INLINE}
```
public static int INLINE
```


Belgeyi tarayıcıya gönderir ve belgeyi diske kaydetme ya da tarayıcı içinde açma seçeneği sunar.

### length {#length}
```
public static int length
```


### fromName(String contentDispositionName) {#fromName-java.lang.String}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getName(int contentDisposition) {#getName-int}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int contentDisposition) {#toString-int}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
