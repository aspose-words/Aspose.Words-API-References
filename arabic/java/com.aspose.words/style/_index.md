---
title: "نمط"
linktitle: "نمط"
second_title: "Aspose.Words لـ Java"
description: "يمثل نمطًا مدمجًا أو معرفًا من قبل المستخدم في Java."
type: docs
weight: 641
url: /ar/java/com.aspose.words/style/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Style implements Cloneable
```

يمثل نمطًا واحدًا مدمجًا أو معرفًا من قبل المستخدم.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Styles and Themes ][Working with Styles and Themes].

 **Examples:** 

يوضح كيفية إنشاء وتطبيق نمط مخصص.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```


[Working with Styles and Themes]: https://docs.aspose.com/words/java/working-with-styles-and-themes/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [equals(Style style)](#equals-com.aspose.words.Style) | يقارن مع النمط المحدد. |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [getAliases()](#getAliases) | يحصل على جميع الأسماء المستعارة لهذا النمط. |
| [getAutomaticallyUpdate()](#getAutomaticallyUpdate) | يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة. |
| [getBaseStyleName()](#getBaseStyleName) | يحصل/يضبط اسم النمط الذي يُستند إليه هذا النمط. |
| [getBuiltIn()](#getBuiltIn) | صحيح إذا كان هذا النمط أحد الأنماط المدمجة في MS Word. |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | يحصل على المستند المالك. |
| [getFont()](#getFont) | يحصل على تنسيق الأحرف للنمط. |
| [getLinkedStyleName()](#getLinkedStyleName) | يحصل/يضبط اسم الـ[Style](../../com.aspose.words/style/) المرتبط بهذا. |
| [getList()](#getList) | يحصل على القائمة التي تحدد تنسيق نمط القائمة هذا. |
| [getListFormat()](#getListFormat) | يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة. |
| [getLocked()](#getLocked) | يحدد ما إذا كان هذا النمط مقفلاً. |
| [getName()](#getName) | يحصل على اسم النمط. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName) | يحصل/يضبط اسم النمط الذي سيُطبق تلقائياً على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد. |
| [getParagraphFormat()](#getParagraphFormat) | يحصل على تنسيق الفقرة للنمط. |
| [getPriority()](#getPriority) | يحصل/يضبط القيمة الصحيحة التي تمثل أولوية فرز الأنماط في لوحة مهام الأنماط. |
| [getSemiHidden()](#getSemiHidden) | يحصل/يضبط ما إذا كان النمط مخفياً في معرض الأنماط ومن لوحة مهام الأنماط. |
| [getStyleIdentifier()](#getStyleIdentifier) | يحصل على معرف النمط المستقل عن اللغة لنمط مدمج. |
| [getStyles()](#getStyles) | يحصل على مجموعة الأنماط التي ينتمي إليها هذا النمط. |
| [getType()](#getType) | يحصل على نوع النمط (فقرة أو حرف). |
| [getUnhideWhenUsed()](#getUnhideWhenUsed) | يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر نفسه في معرض الأنماط ومن لوحة مهام الأنماط. |
| [isHeading()](#isHeading) | صحيح عندما يكون النمط أحد أنماط العناوين المدمجة. |
| [isQuickStyle()](#isQuickStyle) | يحدد ما إذا كان هذا النمط معروضاً في معرض الأنماط السريعة داخل واجهة MS Word. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean) | يحدد ما إذا كان هذا النمط معروضاً في معرض الأنماط السريعة داخل واجهة MS Word. |
| [remove()](#remove) | يزيل النمط المحدد من المستند. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setAutomaticallyUpdate(boolean value)](#setAutomaticallyUpdate-boolean) | يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة. |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String) | يحصل/يضبط اسم النمط الذي يُستند إليه هذا النمط. |
| [setLinkedStyleName(String value)](#setLinkedStyleName-java.lang.String) | يحصل/يضبط اسم الـ[Style](../../com.aspose.words/style/) المرتبط بهذا. |
| [setLocked(boolean value)](#setLocked-boolean) | يحدد ما إذا كان هذا النمط مقفلاً. |
| [setName(String value)](#setName-java.lang.String) | يضبط اسم النمط. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String) | يحصل/يضبط اسم النمط الذي سيُطبق تلقائياً على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setPriority(int value)](#setPriority-int) | يحصل/يضبط القيمة الصحيحة التي تمثل أولوية فرز الأنماط في لوحة مهام الأنماط. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setSemiHidden(boolean value)](#setSemiHidden-boolean) | يحصل/يضبط ما إذا كان النمط مخفياً في معرض الأنماط ومن لوحة مهام الأنماط. |
| [setUnhideWhenUsed(boolean value)](#setUnhideWhenUsed-boolean) | يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر نفسه في معرض الأنماط ومن لوحة مهام الأنماط. |
### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style}
```
public boolean equals(Style style)
```


يقارن بالنمط المحدد. يتم مقارنة معرّفات الأنماط (Istds) للأنماط المدمجة فقط. لا تُضمّن القيم الافتراضية للأنماط في المقارنة. يتم مقارنة النمط الأساسي، والنمط المرتبط، والنمط التالي للفقرة بشكل متكرر.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) |  |

**Returns:**
boolean
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAliases() {#getAliases}
```
public String[] getAliases()
```


يحصل على جميع الأسماء المستعارة لهذا النمط. إذا لم يكن للنمط أي أسماء مستعارة، يتم إرجاع مصفوفة فارغة من السلاسل.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String[] - جميع الأسماء المستعارة لهذا النمط.
### getAutomaticallyUpdate() {#getAutomaticallyUpdate}
```
public boolean getAutomaticallyUpdate()
```


يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة.

 **Remarks:** 

إذا تم ضبط قيمة الخاصية إلى true، يقوم MS Word تلقائياً بإعادة تعريف النمط الحالي عندما يتم تعديل تنسيق الفقرة المناسب.

خاصية AutomaticallyUpdate تنطبق على أنماط الفقرة فقط.

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية إنشاء وتطبيق نمط مخصص.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getBaseStyleName() {#getBaseStyleName}
```
public String getBaseStyleName()
```


يحصل/يضبط اسم النمط الذي يُستند إليه هذا النمط.

 **Remarks:** 

سيكون هذا سلسلة فارغة إذا لم يكن النمط مستندًا إلى أي نمط آخر ويمكن تعيينه كسلسلة فارغة.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getBuiltIn() {#getBuiltIn}
```
public boolean getBuiltIn()
```


صحيح إذا كان هذا النمط أحد الأنماط المدمجة في MS Word.

 **Examples:** 

يوضح كيفية التمييز بين الأنماط المخصصة والأنماط المدمجة.

```

 Document doc = new Document();

 // When we create a document using Microsoft Word, or programmatically using Aspose.Words,
 // the document will come with a collection of styles to apply to its text to modify its appearance.
 // We can access these built-in styles via the document's "Styles" collection.
 // These styles will all have the "BuiltIn" flag set to "true".
 Style style = doc.getStyles().get("Emphasis");

 Assert.assertTrue(style.getBuiltIn());

 // Create a custom style and add it to the collection.
 // Custom styles such as this will have the "BuiltIn" flag set to "false".
 style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 Assert.assertFalse(style.getBuiltIn());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


يحصل على المستند المالك.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### getFont() {#getFont}
```
public Font getFont()
```


يحصل على تنسيق الأحرف للنمط.

 **Remarks:** 

بالنسبة لأنماط القوائم، تُعيد هذه الخاصية null .

 **Examples:** 

يوضح كيفية إنشاء وتطبيق نمط مخصص.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The character formatting of the style.
### getLinkedStyleName() {#getLinkedStyleName}
```
public String getLinkedStyleName()
```


يحصل/يضبط اسم الـ [Style](../../com.aspose.words/style/) المرتبط بهذا. يُعيد سلسلة فارغة إذا لم يتم ربط أي أنماط.

 **Remarks:** 

يسمح فقط بربط نمط الفقرة بنمط الحرف والعكس بالعكس.

ضبط LinkedStyleName للنمط الحالي يؤدي تلقائيًا إلى ضبط LinkedStyleName للنمط المرتبط.

تعيين السلسلة الفارغة يعادل إلغاء ربط النمط المرتبط مسبقًا.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

يوضح كيفية ربط الأنماط ببعضها البعض.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getList() {#getList}
```
public List getList()
```


يحصل على القائمة التي تحدد تنسيق نمط القائمة هذا.

 **Remarks:** 

هذه الخاصية صالحة فقط لأنماط القوائم. بالنسبة لأنواع الأنماط الأخرى تُعيد هذه الخاصية null .

 **Examples:** 

يوضح كيفية إنشاء نمط قائمة واستخدامه في مستند.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // We can contain an entire List object within a style.
 Style listStyle = doc.getStyles().add(StyleType.LIST, "MyListStyle");

 List list1 = listStyle.getList();

 Assert.assertTrue(list1.isListStyleDefinition());
 Assert.assertFalse(list1.isListStyleReference());
 Assert.assertTrue(list1.isMultiLevel());
 Assert.assertEquals(listStyle, list1.getStyle());

 // Change the appearance of all list levels in our list.
 for (ListLevel level : list1.getListLevels()) {
     level.getFont().setName("Verdana");
     level.getFont().setColor(Color.BLUE);
     level.getFont().setBold(true);
 }

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Using list style first time:");

 // Create another list from a list within a style.
 List list2 = doc.getLists().add(listStyle);

 Assert.assertFalse(list2.isListStyleDefinition());
 Assert.assertTrue(list2.isListStyleReference());
 Assert.assertEquals(listStyle, list2.getStyle());

 // Add some list items that our list will format.
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.writeln("Using list style second time:");

 // Create and apply another list based on the list style.
 List list3 = doc.getLists().add(listStyle);
 builder.getListFormat().setList(list3);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateAndUseListStyle.docx");
 
```

**Returns:**
[List](../../com.aspose.words/list/) - The list that defines formatting of this list style.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة.

 **Remarks:** 

هذه الخاصية صالحة فقط لأنماط الفقرات. بالنسبة لأنواع الأنماط الأخرى تُعيد هذه الخاصية null .

 **Examples:** 

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - The corresponding [ListFormat](../../com.aspose.words/listformat/) value.
### getLocked() {#getLocked}
```
public boolean getLocked()
```


يحدد ما إذا كان هذا النمط مقفلاً.

 **Examples:** 

يوضح كيفية قفل النمط.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getName() {#getName}
```
public String getName()
```


يحصل على اسم النمط.

 **Remarks:** 

لا يمكن أن تكون سلسلة فارغة.

إذا كان هناك نمط بالفعل بهذا الاسم في المجموعة، فسيتم استبداله بهذا النمط. جميع العقد المتأثرة ستشير إلى النمط الجديد.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - اسم النمط.
### getNextParagraphStyleName() {#getNextParagraphStyleName}
```
public String getNextParagraphStyleName()
```


يحصل/يضبط اسم النمط الذي سيُطبق تلقائياً على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد.

 **Remarks:** 

هذه الخاصية لا يستخدمها Aspose.Words. سيتم تطبيق نمط الفقرة التالي تلقائيًا فقط عندما تقوم بتحرير المستند في MS Word.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


يحصل على تنسيق الفقرة للنمط.

 **Remarks:** 

بالنسبة لأنماط الحرف والقائمة تُعيد هذه الخاصية null .

 **Examples:** 

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The paragraph formatting of the style.
### getPriority() {#getPriority}
```
public int getPriority()
```


يحصل/يضبط القيمة الصحيحة التي تمثل أولوية فرز الأنماط في لوحة مهام الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
int - القيمة المقابلة  int .
### getSemiHidden() {#getSemiHidden}
```
public boolean getSemiHidden()
```


يحصل/يضبط ما إذا كان النمط مخفياً في معرض الأنماط ومن لوحة مهام الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


يحصل على معرف النمط المستقل عن اللغة لنمط مدمج.

 **Remarks:** 

بالنسبة للأنماط المعرفة من قبل المستخدم (المخصصة)، تُعيد هذه الخاصية [StyleIdentifier.USER](../../com.aspose.words/styleidentifier/\\#USER).

 **Examples:** 

يعرض كيفية تعديل موضع علامة التبويب اليمنى في الفقرات المتعلقة بالفهرس.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
int - معرف النمط المستقل عن اللغة لمظهر مدمج. القيمة المرجعة هي واحدة من ثوابت [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


يحصل على مجموعة الأنماط التي ينتمي إليها هذا النمط.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection/) - The collection of styles this style belongs to.
### getType() {#getType}
```
public int getType()
```


يحصل على نوع النمط (فقرة أو حرف).

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
int - نوع النمط (فقرة أو حرف). القيمة المرجعة هي واحدة من ثوابت [StyleType](../../com.aspose.words/styletype/).
### getUnhideWhenUsed() {#getUnhideWhenUsed}
```
public boolean getUnhideWhenUsed()
```


يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر من معرض الأنماط ومن لوحة مهام الأنماط. True عندما يجب إظهار النمط المستخدم في معرض الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isHeading() {#isHeading}
```
public boolean isHeading()
```


صحيح عندما يكون النمط أحد أنماط العناوين المدمجة.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isQuickStyle() {#isQuickStyle}
```
public boolean isQuickStyle()
```


يحدد ما إذا كان هذا النمط معروضاً في معرض الأنماط السريعة داخل واجهة MS Word.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isQuickStyle(boolean value) {#isQuickStyle-boolean}
```
public void isQuickStyle(boolean value)
```


يحدد ما إذا كان هذا النمط معروضاً في معرض الأنماط السريعة داخل واجهة MS Word.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### remove() {#remove}
```
public void remove()
```


يزيل النمط المحدد من المستند.

 **Remarks:** 

إزالة النمط لها التأثيرات التالية على نموذج المستند:

 *  All references to the style are removed from corresponding paragraphs, runs and tables.
 *  If base style is removed its formatting is moved to child styles.
 *  If style to be deleted has a linked style, then both of these are deleted.

 **Examples:** 

يوضح كيفية إنشاء وتطبيق نمط مخصص.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

### setAutomaticallyUpdate(boolean value) {#setAutomaticallyUpdate-boolean}
```
public void setAutomaticallyUpdate(boolean value)
```


يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة.

 **Remarks:** 

إذا تم ضبط قيمة الخاصية إلى true، يقوم MS Word تلقائياً بإعادة تعريف النمط الحالي عندما يتم تعديل تنسيق الفقرة المناسب.

خاصية AutomaticallyUpdate تنطبق على أنماط الفقرة فقط.

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية إنشاء وتطبيق نمط مخصص.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String}
```
public void setBaseStyleName(String value)
```


يحصل/يضبط اسم النمط الذي يُستند إليه هذا النمط.

 **Remarks:** 

سيكون هذا سلسلة فارغة إذا لم يكن النمط مستندًا إلى أي نمط آخر ويمكن تعيينه كسلسلة فارغة.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setLinkedStyleName(String value) {#setLinkedStyleName-java.lang.String}
```
public void setLinkedStyleName(String value)
```


يحصل/يضبط اسم الـ [Style](../../com.aspose.words/style/) المرتبط بهذا. يُعيد سلسلة فارغة إذا لم يتم ربط أي أنماط.

 **Remarks:** 

يسمح فقط بربط نمط الفقرة بنمط الحرف والعكس بالعكس.

ضبط LinkedStyleName للنمط الحالي يؤدي تلقائيًا إلى ضبط LinkedStyleName للنمط المرتبط.

تعيين السلسلة الفارغة يعادل إلغاء ربط النمط المرتبط مسبقًا.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

يوضح كيفية ربط الأنماط ببعضها البعض.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setLocked(boolean value) {#setLocked-boolean}
```
public void setLocked(boolean value)
```


يحدد ما إذا كان هذا النمط مقفلاً.

 **Examples:** 

يوضح كيفية قفل النمط.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


يضبط اسم النمط.

 **Remarks:** 

لا يمكن أن تكون سلسلة فارغة.

إذا كان هناك نمط بالفعل بهذا الاسم في المجموعة، فسيتم استبداله بهذا النمط. جميع العقد المتأثرة ستشير إلى النمط الجديد.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم النمط. |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String}
```
public void setNextParagraphStyleName(String value)
```


يحصل/يضبط اسم النمط الذي سيُطبق تلقائياً على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد.

 **Remarks:** 

هذه الخاصية لا يستخدمها Aspose.Words. سيتم تطبيق نمط الفقرة التالي تلقائيًا فقط عندما تقوم بتحرير المستند في MS Word.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setPriority(int value) {#setPriority-int}
```
public void setPriority(int value)
```


يحصل/يضبط القيمة الصحيحة التي تمثل أولوية فرز الأنماط في لوحة مهام الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setSemiHidden(boolean value) {#setSemiHidden-boolean}
```
public void setSemiHidden(boolean value)
```


يحصل/يضبط ما إذا كان النمط مخفياً في معرض الأنماط ومن لوحة مهام الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setUnhideWhenUsed(boolean value) {#setUnhideWhenUsed-boolean}
```
public void setUnhideWhenUsed(boolean value)
```


يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر من معرض الأنماط ومن لوحة مهام الأنماط. True عندما يجب إظهار النمط المستخدم في معرض الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

