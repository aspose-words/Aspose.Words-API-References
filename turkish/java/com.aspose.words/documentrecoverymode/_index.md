---
title: "DocumentRecoveryMode"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words Java için"
description: "Bir belge Java'da yüklenirken hatalarla karşılaştığında mevcut kurtarma seçeneklerini belirtir."
type: docs
weight: 171
url: /tr/java/com.aspose.words/documentrecoverymode/
---

**Inheritance:**
java.lang.Object
```
public class DocumentRecoveryMode
```

Bir belge yükleme sırasında hatalarla karşılaştığında kullanılabilir kurtarma seçeneklerini belirtir.

 **Examples:** 

Yükleme sırasında hatalar oluştuysa bir belgeyi kurtarmaya nasıl çalışılacağını gösterir.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [NONE](#NONE) | Kurtarma denenmez. |
| [TRY_RECOVER](#TRY-RECOVER) | Mümkün olduğunca çok veri korunarak belgeyi kurtarmaya çalışır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String documentRecoveryModeName)](#fromName-java.lang.String) |  |
| [getName(int documentRecoveryMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentRecoveryMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Kurtarma denenmez. Belge geçersizse, yükleme bir hata ile başarısız olur.

### TRY_RECOVER {#TRY-RECOVER}
```
public static int TRY_RECOVER
```


Mümkün olduğunca çok veri korunarak belgeyi kurtarmaya çalışır.

### length {#length}
```
public static int length
```


### fromName(String documentRecoveryModeName) {#fromName-java.lang.String}
```
public static int fromName(String documentRecoveryModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentRecoveryModeName | java.lang.String |  |

**Returns:**
int
### getName(int documentRecoveryMode) {#getName-int}
```
public static String getName(int documentRecoveryMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentRecoveryMode) {#toString-int}
```
public static String toString(int documentRecoveryMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
