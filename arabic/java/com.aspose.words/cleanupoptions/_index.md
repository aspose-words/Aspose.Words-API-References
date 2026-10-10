---
title: "CleanupOptions"
linktitle: "CleanupOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات تنظيف المستند في جافا."
type: docs
weight: 103
url: /ar/java/com.aspose.words/cleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class CleanupOptions
```

يسمح بتحديد خيارات لتنظيف المستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Clean Up a Document ][Clean Up a Document].

 **Examples:** 

يعرض كيفية إزالة جميع الأنماط المخصصة غير المستخدمة من المستند.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```


[Clean Up a Document]: https://docs.aspose.com/words/java/clean-up-a-document/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getDuplicateStyle()](#getDuplicateStyle) | يحصل/يضبط علامة تشير إلى ما إذا كان يجب إزالة الأنماط المكررة من المستند. |
| [getUnusedBuiltinStyles()](#getUnusedBuiltinStyles) | يحدد أن الأنماط غير المستخدمة [Style.getBuiltIn()](../../com.aspose.words/style/\#getBuiltIn) يجب إزالتها من المستند. |
| [getUnusedLists()](#getUnusedLists) | يحدد ما إذا كان يجب إزالة القوائم وتعريفات القوائم غير المستخدمة من المستند. |
| [getUnusedStyles()](#getUnusedStyles) | يحدد ما إذا كان يجب إزالة الأنماط غير المستخدمة من المستند. |
| [setDuplicateStyle(boolean value)](#setDuplicateStyle-boolean) | يحصل/يضبط علامة تشير إلى ما إذا كان يجب إزالة الأنماط المكررة من المستند. |
| [setUnusedBuiltinStyles(boolean value)](#setUnusedBuiltinStyles-boolean) | يحدد أن الأنماط غير المستخدمة [Style.getBuiltIn()](../../com.aspose.words/style/\#getBuiltIn) يجب إزالتها من المستند. |
| [setUnusedLists(boolean value)](#setUnusedLists-boolean) | يحدد ما إذا كان يجب إزالة القوائم وتعريفات القوائم غير المستخدمة من المستند. |
| [setUnusedStyles(boolean value)](#setUnusedStyles-boolean) | يحدد ما إذا كان يجب إزالة الأنماط غير المستخدمة من المستند. |
### getDuplicateStyle() {#getDuplicateStyle}
```
public boolean getDuplicateStyle()
```


يحصل/يضبط علامة تشير إلى ما إذا كان يجب إزالة الأنماط المكررة من المستند. القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية إزالة الأنماط المكررة من المستند.

```

 Document doc = new Document();

 // Add two styles to the document with identical properties,
 // but different names. The second style is considered a duplicate of the first.
 Style myStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 Style duplicateStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle2");
 duplicateStyle.getFont().setSize(14.0);
 duplicateStyle.getFont().setName("Courier New");
 duplicateStyle.getFont().setColor(Color.BLUE);

 Assert.assertEquals(6, doc.getStyles().getCount());

 // Apply both styles to different paragraphs within the document.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 builder.getParagraphFormat().setStyleName(duplicateStyle.getName());
 builder.writeln("Hello again!");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(duplicateStyle, paragraphs.get(1).getParagraphFormat().getStyle());

 // Configure a CleanOptions object, then call the Cleanup method to substitute all duplicate styles
 // with the original and remove the duplicates from the document.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setDuplicateStyle(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(5, doc.getStyles().getCount());
 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(myStyle, paragraphs.get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getUnusedBuiltinStyles() {#getUnusedBuiltinStyles}
```
public boolean getUnusedBuiltinStyles()
```


يحدد أن الأنماط غير المستخدمة [Style.getBuiltIn()](../../com.aspose.words/style/\#getBuiltIn) يجب إزالتها من المستند.

 **Examples:** 

يعرض كيفية إزالة جميع الأنماط المخصصة غير المستخدمة من المستند.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getUnusedLists() {#getUnusedLists}
```
public boolean getUnusedLists()
```


يحدد ما إذا كان يجب إزالة القوائم وتعريفات القوائم غير المستخدمة من المستند. القيمة الافتراضية هي true.

 **Examples:** 

يعرض كيفية إزالة جميع الأنماط المخصصة غير المستخدمة من المستند.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getUnusedStyles() {#getUnusedStyles}
```
public boolean getUnusedStyles()
```


يحدد ما إذا كان يجب إزالة الأنماط غير المستخدمة من المستند. القيمة الافتراضية هي true.

 **Examples:** 

يعرض كيفية إزالة جميع الأنماط المخصصة غير المستخدمة من المستند.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### setDuplicateStyle(boolean value) {#setDuplicateStyle-boolean}
```
public void setDuplicateStyle(boolean value)
```


يحصل/يضبط علامة تشير إلى ما إذا كان يجب إزالة الأنماط المكررة من المستند. القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية إزالة الأنماط المكررة من المستند.

```

 Document doc = new Document();

 // Add two styles to the document with identical properties,
 // but different names. The second style is considered a duplicate of the first.
 Style myStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 Style duplicateStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle2");
 duplicateStyle.getFont().setSize(14.0);
 duplicateStyle.getFont().setName("Courier New");
 duplicateStyle.getFont().setColor(Color.BLUE);

 Assert.assertEquals(6, doc.getStyles().getCount());

 // Apply both styles to different paragraphs within the document.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 builder.getParagraphFormat().setStyleName(duplicateStyle.getName());
 builder.writeln("Hello again!");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(duplicateStyle, paragraphs.get(1).getParagraphFormat().getStyle());

 // Configure a CleanOptions object, then call the Cleanup method to substitute all duplicate styles
 // with the original and remove the duplicates from the document.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setDuplicateStyle(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(5, doc.getStyles().getCount());
 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(myStyle, paragraphs.get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setUnusedBuiltinStyles(boolean value) {#setUnusedBuiltinStyles-boolean}
```
public void setUnusedBuiltinStyles(boolean value)
```


يحدد أن الأنماط غير المستخدمة [Style.getBuiltIn()](../../com.aspose.words/style/\#getBuiltIn) يجب إزالتها من المستند.

 **Examples:** 

يعرض كيفية إزالة جميع الأنماط المخصصة غير المستخدمة من المستند.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setUnusedLists(boolean value) {#setUnusedLists-boolean}
```
public void setUnusedLists(boolean value)
```


يحدد ما إذا كان يجب إزالة القوائم وتعريفات القوائم غير المستخدمة من المستند. القيمة الافتراضية هي true.

 **Examples:** 

يعرض كيفية إزالة جميع الأنماط المخصصة غير المستخدمة من المستند.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setUnusedStyles(boolean value) {#setUnusedStyles-boolean}
```
public void setUnusedStyles(boolean value)
```


يحدد ما إذا كان يجب إزالة الأنماط غير المستخدمة من المستند. القيمة الافتراضية هي true.

 **Examples:** 

يعرض كيفية إزالة جميع الأنماط المخصصة غير المستخدمة من المستند.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

