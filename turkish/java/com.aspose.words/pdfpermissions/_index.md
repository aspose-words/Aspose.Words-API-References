---
title: "PdfPermissions"
linktitle: "PdfPermissions"
second_title: "Aspose.Words Java için"
description: "Java'da şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir."
type: docs
weight: 541
url: /tr/java/com.aspose.words/pdfpermissions/
---

**Inheritance:**
java.lang.Object
```
public class PdfPermissions
```

Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir.

 **Examples:** 

Kaydedilmiş bir PDF belgesinde izinlerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ALLOW_ALL](#ALLOW-ALL) | PDF belgesinde tüm işlemlere izin verir. |
| [CONTENT_COPY](#CONTENT-COPY) | Belgeden metin ve grafikleri, [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY) tarafından kontrol edilen işlemler dışındaki işlemlerle kopyalar veya çıkarır. |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | Metin ve grafikleri çıkarır (engelli kullanıcıların erişilebilirliğini desteklemek veya diğer amaçlar için). |
| [DISALLOW_ALL](#DISALLOW-ALL) | PDF belgesinde tüm işlemlere izin vermez. |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) | Belgeyi birleştirir (sayfaları ekler, döndürür veya siler ve belge taslak öğeleri veya küçük resimler oluşturur), [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) temiz olsa bile. |
| [FILL_IN](#FILL-IN) | Mevcut etkileşimli form alanlarını (imza alanları dahil) doldurur, [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) temiz olsa bile. |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | PDF içeriğinin doğru bir dijital kopyası oluşturulabilecek bir temsile belgeyi yazdırır, uygulamaya bağlı bir algoritmaya dayanarak. |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) | Metin açıklamalarını ekler veya değiştirir, etkileşimli form alanlarını doldurur ve [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) de ayarlıysa, etkileşimli form alanlarını (imza alanları dahil) oluşturur veya değiştirir. |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) | Belgenin içeriğini, [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) ve [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY) tarafından kontrol edilen işlemler dışındaki işlemlerle değiştirir. |
| [PRINTING](#PRINTING) | Belgeyi yazdırır (en yüksek kalite seviyesinde olmayabilir, [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) de ayarlı olup olmamasına bağlı olarak). |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set) |  |
| [getName(int pdfPermissions)](#getName-int) |  |
| [getNames(int pdfPermissions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPermissions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


PDF belgesinde tüm işlemlere izin verir.

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


Belgeden metin ve grafikleri, [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY) tarafından kontrol edilen işlemler dışındaki işlemlerle kopyalar veya çıkarır.

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


Metin ve grafikleri çıkarır (engelli kullanıcıların erişilebilirliğini desteklemek veya diğer amaçlar için).

### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


PDF belgesinde tüm işlemlere izin vermez. Bu varsayılan değerdir.

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


Belgeyi birleştirir (sayfaları ekler, döndürür veya siler ve belge taslak öğeleri veya küçük resimler oluşturur), [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) temiz olsa bile.

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


Mevcut etkileşimli form alanlarını (imza alanları dahil) doldurur, [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) temiz olsa bile.

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


PDF içeriğinin doğru bir dijital kopyası oluşturulabilecek bir temsile belgeyi yazdırır, uygulamaya bağlı bir algoritmaya dayanarak. Bu bayrak temiz olduğunda (ve [PRINTING](../../com.aspose.words/pdfpermissions/\#PRINTING) ayarlıysa), yazdırma görünümün düşük seviyeli bir temsiliyle sınırlı olacaktır, muhtemelen kalite kaybıyla.

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


Metin açıklamalarını ekler veya değiştirir, etkileşimli form alanlarını doldurur ve [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) de ayarlıysa, etkileşimli form alanlarını (imza alanları dahil) oluşturur veya değiştirir.

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


Belgenin içeriğini, [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) ve [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY) tarafından kontrol edilen işlemler dışındaki işlemlerle değiştirir.

### PRINTING {#PRINTING}
```
public static int PRINTING
```


Belgeyi yazdırır (en yüksek kalite seviyesinde olmayabilir, [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) de ayarlı olup olmamasına bağlı olarak).

### length {#length}
```
public static int length
```


### fromName(String pdfPermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPermissionsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set pdfPermissionsNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**Returns:**
int
### getName(int pdfPermissions) {#getName-int}
```
public static String getName(int pdfPermissions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int}
```
public static Set getNames(int pdfPermissions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPermissions) {#toString-int}
```
public static String toString(int pdfPermissions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
