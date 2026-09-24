---
title: "WarningType"
linktitle: "WarningType"
second_title: "Aspose.Words Java için"
description: "Java'da belge yükleme veya kaydetme sırasında Aspose.Words tarafından verilen bir uyarının tipini belirtir."
type: docs
weight: 720
url: /tr/java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

Belge yükleme veya kaydetme sırasında Aspose.Words tarafından verilen uyarının türünü belirtir.

 **Examples:** 

Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulmak üzere özelliğin nasıl ayarlanacağını gösterir.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | Genel veri kaybı, belirli bir kod yok. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Yüklemeden sonra belge ağacından veya kaydetmeden sonra oluşturulan belgeden bazı metin/karakter/görsel veya diğer veriler eksik olacaktır. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Belge kaydedilirken gömülü yazı tipi bilgilerinin kaybı. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | Yazı tipi değiştirildi. |
| [HINT](#HINT) | Potansiyel bir sorunu bildirir veya bir iyileştirme önerir. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Genel büyük biçimlendirme kaybı, belirli bir kod yok. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | Ortaya çıkan belge veya içindeki belirli bir konum, orijinal belgeye kıyasla önemli ölçüde farklı görünebilir. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Genel küçük biçimlendirme kaybı, belirli bir kod yok. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | Ortaya çıkan belge veya içindeki belirli bir konum, orijinal belgeye kıyasla biraz farklı görünebilir. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Genel beklenmeyen içerik, belirli bir kod yok. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Kaynak belgede bazı içerikler tanınamadı (örneğin |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String warningTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set) |  |
| [getName(int warningType)](#getName-int) |  |
| [getNames(int warningType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


Genel veri kaybı, belirli bir kod yok.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Yüklemeden sonra belge ağacından veya kaydetmeden sonra oluşturulan belgeden bazı metin/karakter/görsel veya diğer veriler eksik olacaktır.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Belge kaydedilirken gömülü yazı tipi bilgilerinin kaybı.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


Yazı tipi değiştirildi.

### HINT {#HINT}
```
public static int HINT
```


Potansiyel bir sorunu bildirir veya bir iyileştirme önerir.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Genel büyük biçimlendirme kaybı, belirli bir kod yok.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


Ortaya çıkan belge veya içindeki belirli bir konum, orijinal belgeye kıyasla önemli ölçüde farklı görünebilir.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Genel küçük biçimlendirme kaybı, belirli bir kod yok.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


Ortaya çıkan belge veya içindeki belirli bir konum, orijinal belgeye kıyasla biraz farklı görünebilir.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Genel beklenmeyen içerik, belirli bir kod yok.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Kaynak belgede bazı içerikler tanınamadı (örneğin desteklenmiyor), bu sorunlara yol açabilir veya açmayabilir ve veri/biçimlendirme kaybına neden olabilir.

### length {#length}
```
public static int length
```


### fromName(String warningTypeName) {#fromName-java.lang.String}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int warningType) {#getName-int}
```
public static String getName(int warningType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int}
```
public static Set getNames(int warningType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int warningType) {#toString-int}
```
public static String toString(int warningType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| warningType | int |  |

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
