---
title: "DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات إضافية لعملية بناء المستند في Java."
type: docs
weight: 164
url: /ar/java/com.aspose.words/documentbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilderOptions
```

يسمح بتحديد خيارات إضافية لعملية بناء المستند.

 **Examples:** 

يوضح كيفية تجاهل تنسيق الجدول للمحتوى بعد ذلك.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getContextTableFormatting()](#getContextTableFormatting) | صحيح إذا كان التنسيق المطبق على محتوى الجدول لا يؤثر على تنسيق المحتوى الذي يليه. |
| [getDesignMode()](#getDesignMode) | يتطابق مع وضع التصميم في Microsoft Word. |
| [setContextTableFormatting(boolean value)](#setContextTableFormatting-boolean) | صحيح إذا كان التنسيق المطبق على محتوى الجدول لا يؤثر على تنسيق المحتوى الذي يليه. |
| [setDesignMode(boolean value)](#setDesignMode-boolean) | يتطابق مع وضع التصميم في Microsoft Word. |
### getContextTableFormatting() {#getContextTableFormatting}
```
public boolean getContextTableFormatting()
```


صحيح إذا كان التنسيق المطبق على محتوى الجدول لا يؤثر على تنسيق المحتوى الذي يليه. القيمة الافتراضية هي  true .

 **Examples:** 

يوضح كيفية تجاهل تنسيق الجدول للمحتوى بعد ذلك.

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
boolean - القيمة المنطقية المقابلة.
### getDesignMode() {#getDesignMode}
```
public boolean getDesignMode()
```


يتطابق مع وضع التصميم في Microsoft Word.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### setContextTableFormatting(boolean value) {#setContextTableFormatting-boolean}
```
public void setContextTableFormatting(boolean value)
```


صحيح إذا كان التنسيق المطبق على محتوى الجدول لا يؤثر على تنسيق المحتوى الذي يليه. القيمة الافتراضية هي  true .

 **Examples:** 

يوضح كيفية تجاهل تنسيق الجدول للمحتوى بعد ذلك.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setDesignMode(boolean value) {#setDesignMode-boolean}
```
public void setDesignMode(boolean value)
```


يتطابق مع وضع التصميم في Microsoft Word.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

