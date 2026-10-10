---
title: "WarningType"
linktitle: "WarningType"
second_title: "Aspose.Words для Java"
description: "Указывает тип предупреждения, выдаваемого Aspose.Words при загрузке или сохранении документа в Java."
type: docs
weight: 720
url: /ru/java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

Указывает тип предупреждения, выдаваемого Aspose.Words при загрузке или сохранении документа.

 **Examples:** 

Показывает, как установить свойство для поиска наиболее подходящего шрифта, отсутствующего в системе, среди доступных источников шрифтов.

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
## Поля

| Поле | Описание |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | Общая потеря данных, без конкретного кода. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Некоторый текст/символ/изображение или другие данные будут отсутствовать либо в дереве документа после загрузки, либо в созданном документе после сохранения. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Потеря встроенной информации о шрифте при сохранении документа. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | Шрифт был заменён. |
| [HINT](#HINT) | Сообщает о потенциальной проблеме или предлагает улучшение. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Общая серьёзная потеря форматирования, без конкретного кода. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | Получившийся документ или конкретное место в нём могут выглядеть существенно иначе по сравнению с оригинальным документом. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Общая незначительная потеря форматирования, без конкретного кода. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | Получившийся документ или конкретное место в нём могут выглядеть несколько иначе по сравнению с оригинальным документом. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Общее неожиданное содержимое, без конкретного кода. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Некоторое содержимое исходного документа не удалось распознать (т.е. |
| [length](#length) |  |
## Методы

| Метод | Описание |
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


Общая потеря данных, без конкретного кода.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Некоторый текст/символ/изображение или другие данные будут отсутствовать либо в дереве документа после загрузки, либо в созданном документе после сохранения.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Потеря встроенной информации о шрифте при сохранении документа.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


Шрифт был заменён.

### HINT {#HINT}
```
public static int HINT
```


Сообщает о потенциальной проблеме или предлагает улучшение.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Общая серьёзная потеря форматирования, без конкретного кода.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


Получившийся документ или конкретное место в нём могут выглядеть существенно иначе по сравнению с оригинальным документом.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Общая незначительная потеря форматирования, без конкретного кода.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


Получившийся документ или конкретное место в нём могут выглядеть несколько иначе по сравнению с оригинальным документом.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Общее неожиданное содержимое, без конкретного кода.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Некоторое содержимое исходного документа не удалось распознать (т.е. не поддерживается), это может привести к проблемам или к потере данных/форматирования, а может и не привести.

### length {#length}
```
public static int length
```


### fromName(String warningTypeName) {#fromName-java.lang.String}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int warningType) {#getName-int}
```
public static String getName(int warningType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int}
```
public static Set getNames(int warningType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
