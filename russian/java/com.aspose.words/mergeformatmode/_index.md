---
title: "MergeFormatMode"
linktitle: "MergeFormatMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как объединяется форматирование при комбинировании нескольких документов в Java."
type: docs
weight: 464
url: /ru/java/com.aspose.words/mergeformatmode/
---

**Inheritance:**
java.lang.Object
```
public class MergeFormatMode
```

Указывает, как форматирование объединяется при комбинировании нескольких документов.

 **Examples:** 

Показывает, как объединять документы в один выходной документ.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Означает, что исходный документ сохранит своё оригинальное форматирование, такое как стили шрифтов, размеры, цвета, отступы и любые другие элементы форматирования, применённые к его содержимому. |
| [KEEP_SOURCE_LAYOUT](#KEEP-SOURCE-LAYOUT) | Сохранить макет оригинальных документов в итоговом документе. |
| [MERGE_FORMATTING](#MERGE-FORMATTING) | Объединить форматирование объединённых документов. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String mergeFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int mergeFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFormatMode)](#toString-int) |  |
### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Означает, что исходный документ сохранит своё оригинальное форматирование, такое как стили шрифтов, размеры, цвета, отступы и любые другие элементы форматирования, применённые к его содержимому.

 **Remarks:** 

Используя эту опцию, вы гарантируете, что скопированный контент выглядит так же, как в оригинальном источнике, независимо от настроек форматирования первого документа в очереди объединения.

Эта опция не оказывает никакого влияния, когда входные и выходные форматы являются PDF.

### KEEP_SOURCE_LAYOUT {#KEEP-SOURCE-LAYOUT}
```
public static int KEEP_SOURCE_LAYOUT
```


Сохранить макет оригинальных документов в итоговом документе.

 **Remarks:** 

В общем, это выглядит так, будто вы распечатываете оригинальные документы и вручную склеиваете их вместе с помощью клея.

### MERGE_FORMATTING {#MERGE-FORMATTING}
```
public static int MERGE_FORMATTING
```


Объединить форматирование объединённых документов.

 **Remarks:** 

Используя эту опцию, Aspose.Words адаптирует форматирование первого документа, чтобы оно соответствовало структуре и внешнему виду второго документа, но сохраняет часть оригинального форматирования неизменным. Эта опция полезна, когда вы хотите сохранить общий вид и ощущение целевого документа, но при этом сохранить некоторые аспекты форматирования из оригинального документа.

Эта опция не оказывает никакого влияния, когда входные и выходные форматы являются PDF.

### length {#length}
```
public static int length
```


### fromName(String mergeFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFormatModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mergeFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFormatMode) {#getName-int}
```
public static String getName(int mergeFormatMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFormatMode) {#toString-int}
```
public static String toString(int mergeFormatMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
