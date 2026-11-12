---
title: "ReportBuildOptions"
linktitle: "ReportBuildOptions"
second_title: "Aspose.Words для Java"
description: "Указывает параметры, контролирующие поведение ReportingEngine при построении отчёта в Java."
type: docs
weight: 570
url: /ru/java/com.aspose.words/reportbuildoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuildOptions
```

Указывает параметры, контролирующие поведение [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта.
## Поля

| Поле | Описание |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | Указывает, что отсутствующие члены объекта должны рассматриваться движком как литералы null. |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | Указывает, что движок должен внедрять сообщения об ошибках синтаксиса шаблона непосредственно в выходные документы. |
| [NONE](#NONE) | Указывает параметры по умолчанию. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Указывает, что движок должен удалять абзацы, ставшие пустыми после удаления тегов синтаксиса шаблона или их замены пустыми значениями. |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) | Указывает, что движок должен использовать значения ориентации изображения EXIF \\u200b\\u200bimage для корректного поворота вставленных JPEG‑изображений. |
| [UPDATE_FIELDS_SYNTAX_AWARE](#UPDATE-FIELDS-SYNTAX-AWARE) | Указывает, что движок должен игнорировать синтаксис шаблона в результатах полей и обновлять поля после построения отчёта. |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | Указывает, что движок должен посещать дочерние узлы раздела (заголовки, колонтитулы, тела) в порядке, совместимом с версиями Aspose.Words до 21.9. |
| [length](#length) |  |
## Методы

| Метод | Описание |
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


Указывает, что отсутствующие члены объекта должны рассматриваться движком как литералы null. Эта опция влияет только на доступ к членам экземпляра (то есть нестатическим) объекта и методам расширения. Если эта опция не установлена, движок генерирует исключение при обнаружении отсутствующего члена объекта.

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


Указывает, что движок должен внедрять сообщения об ошибках синтаксиса шаблона непосредственно в выходные документы. Если эта опция не установлена, движок генерирует исключение при обнаружении синтаксической ошибки.

### NONE {#NONE}
```
public static int NONE
```


Указывает параметры по умолчанию.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Указывает, что движок должен удалять абзацы, ставшие пустыми после удаления тегов синтаксиса шаблона или их замены пустыми значениями.

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


Указывает, что движок должен использовать значения ориентации изображения EXIF \\u200b\\u200bimage для корректного поворота вставленных JPEG‑изображений.

### UPDATE_FIELDS_SYNTAX_AWARE {#UPDATE-FIELDS-SYNTAX-AWARE}
```
public static int UPDATE_FIELDS_SYNTAX_AWARE
```


Указывает, что движок должен игнорировать синтаксис шаблона в результатах полей и обновлять поля после построения отчёта.

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


Указывает, что движок должен посещать дочерние узлы раздела (заголовки, колонтитулы, тела) в порядке, совместимом с версиями Aspose.Words до 21.9.

 **Remarks:** 

По умолчанию движок рассматривает заголовки и колонтитулы так, как будто они связаны с разрывами разделов. То есть при посещении дочерних узлов раздела сначала посещается тело, и только затем — заголовки и колонтитулы. Это соответствует поведению Microsoft Word при копировании/вставке или удалении содержимого нескольких разделов и дает более корректные результаты в большинстве сценариев.

До версии Aspose.Words 21.9 движок использовал иной порядок обхода: дочерние узлы раздела посещались в том порядке, в котором они находятся в документе. Примените это значение к [ReportingEngine.getOptions()](../../com.aspose.words/reportingengine/#getOptions) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine/#setOptions-int), если требуется совместимость со старыми версиями Aspose.Words.

### length {#length}
```
public static int length
```


### fromName(String reportBuildOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String reportBuildOptionsName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int reportBuildOptions) {#getName-int}
```
public static String getName(int reportBuildOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int}
```
public static Set getNames(int reportBuildOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
