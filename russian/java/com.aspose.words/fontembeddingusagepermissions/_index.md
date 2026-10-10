---
title: "FontEmbeddingUsagePermissions"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words для Java"
description: "Представляет разрешения на использование встраивания шрифтов в Java."
type: docs
weight: 322
url: /ru/java/com.aspose.words/fontembeddingusagepermissions/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingUsagePermissions
```

Представляет разрешения на использование встраивания шрифта.

 **Examples:** 

Показывает, как получить информацию о правах лицензии для внедрённых шрифтов (FontInfo).

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
## Поля

| Поле | Описание |
| --- | --- |
| [EDITABLE](#EDITABLE) | Шрифт может быть встроен и временно загружен на другие системы. |
| [INSTALLABLE](#INSTALLABLE) | Шрифт может быть встроен и постоянно установлен для использования на удалённых системах или другими пользователями. |
| [PRINT_AND_PREVIEW](#PRINT-AND-PREVIEW) | Шрифт может быть встроен и временно загружен на другие системы для просмотра или печати документа. |
| [RESTRICTED_LICENSE](#RESTRICTED-LICENSE) | Шрифт не должен изменяться, встраиваться или передаваться каким-либо образом без предварительного получения явного разрешения законного владельца. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String fontEmbeddingUsagePermissionsName)](#fromName-java.lang.String) |  |
| [getName(int fontEmbeddingUsagePermissions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontEmbeddingUsagePermissions)](#toString-int) |  |
### EDITABLE {#EDITABLE}
```
public static int EDITABLE
```


Шрифт может быть встроен и временно загружен на другие системы.

 **Remarks:** 

Как и при встраивании для предварительного просмотра и печати, документы, содержащие редактируемые шрифты, могут быть открыты для чтения. Кроме того, разрешено редактирование, включая возможность форматировать новый текст с использованием встроенного шрифта, и изменения могут быть сохранены.

### INSTALLABLE {#INSTALLABLE}
```
public static int INSTALLABLE
```


Шрифт может быть встроен и постоянно установлен для использования на удалённых системах или другими пользователями.

### PRINT_AND_PREVIEW {#PRINT-AND-PREVIEW}
```
public static int PRINT_AND_PREVIEW
```


Шрифт может быть встроен и временно загружен на другие системы для просмотра или печати документа.

 **Remarks:** 

Документы, содержащие шрифты для предварительного просмотра и печати, должны быть открыты \\u201cread-only\\u201d; к документу нельзя применять правки.

### RESTRICTED_LICENSE {#RESTRICTED-LICENSE}
```
public static int RESTRICTED_LICENSE
```


Шрифт не должен изменяться, встраиваться или передаваться каким-либо образом без предварительного получения явного разрешения законного владельца.

### length {#length}
```
public static int length
```


### fromName(String fontEmbeddingUsagePermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String fontEmbeddingUsagePermissionsName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontEmbeddingUsagePermissionsName | java.lang.String |  |

**Returns:**
int
### getName(int fontEmbeddingUsagePermissions) {#getName-int}
```
public static String getName(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
