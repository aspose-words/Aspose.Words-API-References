---
title: "FontEmbeddingUsagePermissions"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words Java için"
description: "Java'da font gömme kullanım izinlerini temsil eder."
type: docs
weight: 322
url: /tr/java/com.aspose.words/fontembeddingusagepermissions/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingUsagePermissions
```

Yazı tipi gömme kullanım izinlerini temsil eder.

 **Examples:** 

Gömülü yazı tipleri için lisans hakları bilgilerini (FontInfo) nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Embedded font rights.docx");

 // Get the list of document fonts.
 FontInfoCollection fontInfos = doc.getFontInfos();
 for (FontInfo fontInfo : fontInfos)
 {
     if (fontInfo.getEmbeddingLicensingRights() != null)
     {
         System.out.println(fontInfo.getEmbeddingLicensingRights().getEmbeddingUsagePermissions());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getBitmapEmbeddingOnly());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getNoSubsetting());
     }
 }
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [EDITABLE](#EDITABLE) | Font gömülebilir ve diğer sistemlerde geçici olarak yüklenebilir. |
| [INSTALLABLE](#INSTALLABLE) | Font gömülebilir ve uzak sistemlerde kullanım için kalıcı olarak kurulabilir veya diğer kullanıcılar tarafından kullanılabilir. |
| [PRINT_AND_PREVIEW](#PRINT-AND-PREVIEW) | Font gömülebilir ve belgeyi görüntüleme veya yazdırma amaçlarıyla diğer sistemlerde geçici olarak yüklenebilir. |
| [RESTRICTED_LICENSE](#RESTRICTED-LICENSE) | Font, yasal sahibinin açık izni alınmadan hiçbir şekilde değiştirilmemeli, gömülmemeli veya değiş tokuş edilmemelidir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String fontEmbeddingUsagePermissionsName)](#fromName-java.lang.String) |  |
| [getName(int fontEmbeddingUsagePermissions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontEmbeddingUsagePermissions)](#toString-int) |  |
### EDITABLE {#EDITABLE}
```
public static int EDITABLE
```


Font gömülebilir ve diğer sistemlerde geçici olarak yüklenebilir.

 **Remarks:** 

Önizleme ve Yazdırma gömme işlemleri gibi, Düzenlenebilir fontları içeren belgeler okuma amaçlı açılabilir. Ayrıca, gömülü fontu kullanarak yeni metni biçimlendirme dahil düzenleme izni verilir ve değişiklikler kaydedilebilir.

### INSTALLABLE {#INSTALLABLE}
```
public static int INSTALLABLE
```


Font gömülebilir ve uzak sistemlerde kullanım için kalıcı olarak kurulabilir veya diğer kullanıcılar tarafından kullanılabilir.

### PRINT_AND_PREVIEW {#PRINT-AND-PREVIEW}
```
public static int PRINT_AND_PREVIEW
```


Font gömülebilir ve belgeyi görüntüleme veya yazdırma amaçlarıyla diğer sistemlerde geçici olarak yüklenebilir.

 **Remarks:** 

Önizleme ve Yazdırma fontlarını içeren belgeler \u201cyalnızca okuma\u201d modunda açılmalıdır; belgeye hiçbir düzenleme uygulanamaz.

### RESTRICTED_LICENSE {#RESTRICTED-LICENSE}
```
public static int RESTRICTED_LICENSE
```


Font, yasal sahibinin açık izni alınmadan hiçbir şekilde değiştirilmemeli, gömülmemeli veya değiş tokuş edilmemelidir.

### length {#length}
```
public static int length
```


### fromName(String fontEmbeddingUsagePermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String fontEmbeddingUsagePermissionsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontEmbeddingUsagePermissionsName | java.lang.String |  |

**Returns:**
int
### getName(int fontEmbeddingUsagePermissions) {#getName-int}
```
public static String getName(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontEmbeddingUsagePermissions) {#toString-int}
```
public static String toString(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
