---
title: "DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Aspose.Words для Java"
description: "Позволяет указать дополнительные параметры процесса построения документа в Java."
type: docs
weight: 164
url: /ru/java/com.aspose.words/documentbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilderOptions
```

Позволяет указать дополнительные параметры процесса построения документа.

 **Examples:** 

Показывает, как игнорировать форматирование таблицы для последующего содержимого.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [getContextTableFormatting()](#getContextTableFormatting) | True, если применённое к содержимому таблицы форматирование не влияет на форматирование последующего содержимого. |
| [getDesignMode()](#getDesignMode) | Соответствует режиму Design Mode в Microsoft Word. |
| [setContextTableFormatting(boolean value)](#setContextTableFormatting-boolean) | True, если применённое к содержимому таблицы форматирование не влияет на форматирование последующего содержимого. |
| [setDesignMode(boolean value)](#setDesignMode-boolean) | Соответствует режиму Design Mode в Microsoft Word. |
### getContextTableFormatting() {#getContextTableFormatting}
```
public boolean getContextTableFormatting()
```


True, если применённое к содержимому таблицы форматирование не влияет на форматирование последующего содержимого. Значение по умолчанию — true.

 **Examples:** 

Показывает, как игнорировать форматирование таблицы для последующего содержимого.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getDesignMode() {#getDesignMode}
```
public boolean getDesignMode()
```


Соответствует режиму Design Mode в Microsoft Word.

**Returns:**
boolean - Соответствующее  boolean  значение.
### setContextTableFormatting(boolean value) {#setContextTableFormatting-boolean}
```
public void setContextTableFormatting(boolean value)
```


True, если применённое к содержимому таблицы форматирование не влияет на форматирование последующего содержимого. Значение по умолчанию — true.

 **Examples:** 

Показывает, как игнорировать форматирование таблицы для последующего содержимого.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setDesignMode(boolean value) {#setDesignMode-boolean}
```
public void setDesignMode(boolean value)
```


Соответствует режиму Design Mode в Microsoft Word.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

