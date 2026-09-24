---
title: "PdfCompliance"
linktitle: "PdfCompliance"
second_title: "Aspose.Words Java için"
description: "Java'da PDF standart uyumluluk seviyesini belirtir."
type: docs
weight: 529
url: /tr/java/com.aspose.words/pdfcompliance/
---

**Inheritance:**
java.lang.Object
```
public class PdfCompliance
```

PDF standart uyumluluk seviyesini belirtir.

 **Examples:** 

Kaydedilen PDF belgelerinin PDF standart uyumluluk seviyesini ayarlamayı gösterir.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Note that some PdfSaveOptions are prohibited when saving to one of the standards and automatically fixed.
 // Use IWarningCallback to know which options are automatically fixed.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "Compliance" property to "PdfCompliance.PdfA1b" to comply with the "PDF/A-1b" standard,
 // which aims to preserve the visual appearance of the document as Aspose.Words convert it to PDF.
 // Set the "Compliance" property to "PdfCompliance.Pdf17" to comply with the "1.7" standard.
 // Set the "Compliance" property to "PdfCompliance.PdfA1a" to comply with the "PDF/A-1a" standard,
 // which complies with "PDF/A-1b" as well as preserving the document structure of the original document.
 // Set the "Compliance" property to "PdfCompliance.PdfUa1" to comply with the "PDF/UA-1" (ISO 14289-1) standard,
 // which aims to define represent electronic documents in PDF that allow the file to be accessible.
 // Set the "Compliance" property to "PdfCompliance.Pdf20" to comply with the "PDF 2.0" (ISO 32000-2) standard.
 // Set the "Compliance" property to "PdfCompliance.PdfA4" to comply with the "PDF/A-4" (ISO 19004:2020) standard,
 // which preserving document static visual appearance over time.
 // Set the "Compliance" property to "PdfCompliance.PdfA4Ua2" to comply with both PDF/A-4 (ISO 19005-4:2020)
 // and PDF/UA-2 (ISO 14289-2:2024) standards.
 // Set the "Compliance" property to "PdfCompliance.PdfUa2" to comply with the PDF/UA-2 (ISO 14289-2:2024) standard.
 // This helps with making documents searchable but may significantly increase the size of already large documents.
 saveOptions.setCompliance(pdfCompliance);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Compliance.pdf", saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [PDF_17](#PDF-17) | Çıktı dosyası PDF 1.7 (ISO 32000-1) standardına uyacaktır. |
| [PDF_20](#PDF-20) | Çıktı dosyası PDF 2.0 (ISO 32000-2) standardına uyacaktır. |
| [PDF_A_1_A](#PDF-A-1-A) | Çıktı dosyası PDF/A-1a (ISO 19005-1) standardına uyacaktır. |
| [PDF_A_1_B](#PDF-A-1-B) | Çıktı dosyası PDF/A-1b (ISO 19005-1) standardına uyacaktır. |
| [PDF_A_2_A](#PDF-A-2-A) | Çıktı dosyası PDF/A-2a (ISO 19005-2) standardına uyacaktır. |
| [PDF_A_2_U](#PDF-A-2-U) | Çıktı dosyası PDF/A-2u (ISO 19005-2) standardına uyacaktır. |
| [PDF_A_3_A](#PDF-A-3-A) | Çıktı dosyası PDF/A-3a (ISO 19005-3) standardına uyacaktır. |
| [PDF_A_3_U](#PDF-A-3-U) | Çıktı dosyası PDF/A-3u (ISO 19005-3) standardına uyacaktır. |
| [PDF_A_4](#PDF-A-4) | Çıktı dosyası PDF/A-4 (ISO 19005-4:2020) standardına uyacaktır. |
| [PDF_A_4_F](#PDF-A-4-F) | Çıktı dosyası PDF/A-4f (ISO 19005-4:2020) standardına uyacaktır. |
| [PDF_A_4_UA_2](#PDF-A-4-UA-2) | Çıktı dosyası hem PDF/A-4 (ISO 19005-4:2020) hem de PDF/UA-2 (ISO 14289-2:2024) standartlarına uyacaktır. |
| [PDF_UA_1](#PDF-UA-1) | Çıktı dosyası PDF/UA-1 (ISO 14289-1) standardına uyacaktır. |
| [PDF_UA_2](#PDF-UA-2) | Çıktı dosyası PDF/UA-2 (ISO 14289-2:2024) standardına uyacaktır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String) |  |
| [getName(int pdfCompliance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCompliance)](#toString-int) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


Çıktı dosyası PDF 1.7 (ISO 32000-1) standardına uyacaktır.

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


Çıktı dosyası PDF 2.0 (ISO 32000-2) standardına uyacaktır.

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


Çıktı dosyası PDF/A-1a (ISO 19005-1) standardına uyacaktır. Bu seviye, PDF/A-1b'nin tüm gereksinimlerini içerir ve ayrıca belge yapısının ("tagged" olarak da bilinir) dahil edilmesini gerektirir; amacı belge içeriğinin aranabilir ve yeniden kullanılabilir olmasını sağlamaktır.

 **Remarks:** 

Belge yapısını dışa aktarmanın bellek tüketimini önemli ölçüde artırdığını, özellikle büyük belgeler için, unutmayın.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


Çıktı dosyası PDF/A-1b (ISO 19005-1) standardına uyacaktır. PDF/A-1b, belgenin görsel görünümünün güvenilir bir şekilde yeniden üretilmesini sağlamayı amaçlar.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


Çıktı dosyası PDF/A-2a (ISO 19005-2) standardına uyacaktır. Bu seviye, PDF/A-2u'nun tüm gereksinimlerini içerir ve ayrıca belge yapısının ("tagged" olarak da bilinir) dahil edilmesini gerektirir; amacı belge içeriğinin aranabilir ve yeniden kullanılabilir olmasını sağlamaktır.

 **Remarks:** 

Belge yapısını dışa aktarmanın bellek tüketimini önemli ölçüde artırdığını, özellikle büyük belgeler için, unutmayın.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


Çıktı dosyası PDF/A-2u (ISO 19005-2) standardına uyacaktır. PDF/A-2u, dosyaların oluşturulması, depolanması veya işlenmesi için kullanılan araç ve sistemlerden bağımsız olarak belgenin statik görsel görünümünün zaman içinde korunmasını amaçlar. Ayrıca, belgede bulunan tüm metin, Unicode kod noktaları dizisi olarak güvenilir bir şekilde çıkarılabilir.

### PDF_A_3_A {#PDF-A-3-A}
```
public static int PDF_A_3_A
```


Çıktı dosyası PDF/A-3a (ISO 19005-3) standardına uyacaktır. Bu seviye, PDF/A-3u'nun tüm gereksinimlerini içerir ve ayrıca belge yapısının ("tagged" olarak da bilinir) dahil edilmesini gerektirir; amacı belge içeriğinin aranabilir ve yeniden kullanılabilir olmasını sağlamaktır.

 **Remarks:** 

Belge yapısını dışa aktarmanın bellek tüketimini önemli ölçüde artırdığını, özellikle büyük belgeler için, unutmayın.

### PDF_A_3_U {#PDF-A-3-U}
```
public static int PDF_A_3_U
```


Çıktı dosyası PDF/A-3u (ISO 19005-3) standardına uyacaktır. PDF/A-3u (PDF/A-2u gibi) dosyaların oluşturulması, depolanması veya işlenmesi için kullanılan araç ve sistemlerden bağımsız olarak belgenin statik görsel görünümünün zaman içinde korunmasını amaçlar. Ayrıca, belgede bulunan tüm metin, Unicode kod noktaları dizisi olarak güvenilir bir şekilde çıkarılabilir. PDF/A-2u'ya ek olarak, PDF/A-3u PDF belgesine ek dosyalar gömmeye izin verir.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


Çıktı dosyası PDF/A-4 (ISO 19005-4:2020) standardına uyacaktır. PDF/A-4, dosyaların oluşturulması, depolanması veya işlenmesi için kullanılan araç ve sistemlerden bağımsız olarak belgenin statik görsel görünümünün zaman içinde korunmasını amaçlar. Ayrıca, belgede bulunan tüm metin, Unicode kod noktaları dizisi olarak güvenilir bir şekilde çıkarılabilir.

### PDF_A_4_F {#PDF-A-4-F}
```
public static int PDF_A_4_F
```


Çıktı dosyası PDF/A-4f (ISO 19005-4:2020) standardına uyacaktır. Bu seviye, PDF/A-4'ün tüm gereksinimlerini içerir ve ayrıca PDF belgesine ek dosyalar gömmeye izin verir.

### PDF_A_4_UA_2 {#PDF-A-4-UA-2}
```
public static int PDF_A_4_UA_2
```


Çıktı dosyası hem PDF/A-4 (ISO 19005-4:2020) hem de PDF/UA-2 (ISO 14289-2:2024) standartlarına uyacaktır. PDF/A-4, dosyaların oluşturulması, depolanması veya işlenmesi için kullanılan araç ve sistemlerden bağımsız olarak belgenin statik görsel görünümünün zaman içinde korunmasını amaçlar. PDF/UA'nın temel amacı, PDF formatında elektronik belgelerin erişilebilir olmasını sağlayacak şekilde temsil edilme şeklini tanımlamaktır.

 **Remarks:** 

Belge yapısını dışa aktarmanın bellek tüketimini önemli ölçüde artırdığını, özellikle büyük belgeler için, unutmayın.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


Çıktı dosyası PDF/UA-1 (ISO 14289-1) standardına uygun olacaktır. PDF/UA'nın temel amacı, elektronik belgelerin PDF formatında nasıl temsil edileceğini, dosyanın erişilebilir olmasını sağlayacak şekilde tanımlamaktır.

 **Remarks:** 

Belge yapısını dışa aktarmanın bellek tüketimini önemli ölçüde artırdığını, özellikle büyük belgeler için, unutmayın.

### PDF_UA_2 {#PDF-UA-2}
```
public static int PDF_UA_2
```


Çıktı dosyası PDF/UA-2 (ISO 14289-2:2024) standardına uygun olacaktır. PDF/UA'nın temel amacı, elektronik belgelerin PDF formatında nasıl temsil edileceğini, dosyanın erişilebilir olmasını sağlayacak şekilde tanımlamaktır.

 **Remarks:** 

Belge yapısını dışa aktarmanın bellek tüketimini önemli ölçüde artırdığını, özellikle büyük belgeler için, unutmayın.

### length {#length}
```
public static int length
```


### fromName(String pdfComplianceName) {#fromName-java.lang.String}
```
public static int fromName(String pdfComplianceName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCompliance) {#getName-int}
```
public static String getName(int pdfCompliance)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfCompliance) {#toString-int}
```
public static String toString(int pdfCompliance)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
