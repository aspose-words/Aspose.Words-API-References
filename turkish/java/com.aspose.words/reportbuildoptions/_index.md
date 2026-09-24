---
title: "ReportBuildOptions"
linktitle: "ReportBuildOptions"
second_title: "Aspose.Words Java için"
description: "Java'da rapor oluştururken ReportingEngine'in davranışını kontrol eden seçenekleri belirtir."
type: docs
weight: 570
url: /tr/java/com.aspose.words/reportbuildoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuildOptions
```

Rapor oluştururken [ReportingEngine](../../com.aspose.words/reportingengine/) davranışını kontrol eden seçenekleri belirtir.
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | Eksik nesne üyelerinin motor tarafından null sabitleri olarak ele alınması gerektiğini belirtir. |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | Motorun şablon sözdizimi hata mesajlarını çıktı belgelerine satır içi eklemesi gerektiğini belirtir. |
| [NONE](#NONE) | Varsayılan seçenekleri belirtir. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Motorun, şablon sözdizimi etiketleri kaldırıldıktan veya boş değerlerle değiştirildikten sonra boş kalan paragrafları kaldırması gerektiğini belirtir. |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) | Motorun, eklenen JPEG görüntülerini uygun şekilde döndürmek için EXIF \\u200b\\u200bimage orientation değerlerini kullanması gerektiğini belirtir. |
| [UPDATE_FIELDS_SYNTAX_AWARE](#UPDATE-FIELDS-SYNTAX-AWARE) | Motorun, alan sonuçlarındaki şablon sözdizimini yok sayması ve rapor oluşturulduktan sonra alanları güncellemesi gerektiğini belirtir. |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | Motorun, bölüm alt düğümlerini (başlıklar, altbilgiler, gövdeler) Aspose.Words 21.9 öncesi sürümlerle uyumlu bir sırada ziyaret etmesi gerektiğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String reportBuildOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set reportBuildOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int reportBuildOptions)](#getName-int) |  |
| [getNames(int reportBuildOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int reportBuildOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_MISSING_MEMBERS {#ALLOW-MISSING-MEMBERS}
```
public static int ALLOW_MISSING_MEMBERS
```


Motorun eksik nesne üyelerini null sabitleri olarak ele alması gerektiğini belirtir. Bu seçenek yalnızca örnek (yani statik olmayan) nesne üyelerine ve uzantı yöntemlerine erişimi etkiler. Bu seçenek ayarlanmamışsa, motor eksik bir nesne üyesiyle karşılaştığında bir istisna fırlatır.

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


Motorun şablon sözdizimi hata mesajlarını çıktı belgelerine satır içi eklemesi gerektiğini belirtir. Bu seçenek ayarlanmamışsa, motor bir sözdizimi hatasıyla karşılaştığında bir istisna fırlatır.

### NONE {#NONE}
```
public static int NONE
```


Varsayılan seçenekleri belirtir.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Motorun, şablon sözdizimi etiketleri kaldırıldıktan veya boş değerlerle değiştirildikten sonra boş kalan paragrafları kaldırması gerektiğini belirtir.

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


Motorun, eklenen JPEG görüntülerini uygun şekilde döndürmek için EXIF \\u200b\\u200bimage orientation değerlerini kullanması gerektiğini belirtir.

### UPDATE_FIELDS_SYNTAX_AWARE {#UPDATE-FIELDS-SYNTAX-AWARE}
```
public static int UPDATE_FIELDS_SYNTAX_AWARE
```


Motorun, alan sonuçlarındaki şablon sözdizimini yok sayması ve rapor oluşturulduktan sonra alanları güncellemesi gerektiğini belirtir.

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


Motorun, bölüm alt düğümlerini (başlıklar, altbilgiler, gövdeler) Aspose.Words 21.9 öncesi sürümlerle uyumlu bir sırada ziyaret etmesi gerektiğini belirtir.

 **Remarks:** 

Varsayılan olarak, motor başlıkları ve altbilgileri bölüm sonlarına bağlıymış gibi ele alır. Yani, bölüm alt düğümleri ziyaret ederken önce gövde ziyaret edilir, ardından başlıklar ve altbilgiler ziyaret edilir. Bu, Microsoft Word'ün çok bölümlü içerikleri kopyalayıp yapıştırma veya kaldırma davranışıyla uyumludur ve çoğu senaryoda daha doğru sonuçlar üretir.

Aspose.Words 21.9 öncesinde, motor başka bir ziyaret sırası kullanıyordu: Bölüm alt düğümleri belgede göründükleri sırayla ziyaret ediliyordu. Aspose.Words'ün eski sürümleriyle uyumluluk gerekiyorsa bu değeri [ReportingEngine.getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) metodlarına uygulayın.

### length {#length}
```
public static int length
```


### fromName(String reportBuildOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String reportBuildOptionsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int reportBuildOptions) {#getName-int}
```
public static String getName(int reportBuildOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int}
```
public static Set getNames(int reportBuildOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int reportBuildOptions) {#toString-int}
```
public static String toString(int reportBuildOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
