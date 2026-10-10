---
title: "StyleCollection"
linktitle: "StyleCollection"
second_title: "Aspose.Words لـ Java"
description: "مجموعة من كائنات Style التي تمثل كل من الأنماط المدمجة والمحددة من قبل المستخدم في مستند بلغة Java."
type: docs
weight: 642
url: /ar/java/com.aspose.words/stylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

مجموعة من كائنات [Style](../../com.aspose.words/style/) التي تمثل كل من الأنماط المدمجة والمحددة من قبل المستخدم في مستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Styles and Themes ][Working with Styles and Themes].

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


[Working with Styles and Themes]: https://docs.aspose.com/words/java/working-with-styles-and-themes/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(int type, String name)](#add-int-java.lang.String) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style) | ينسخ نمطًا إلى هذه المجموعة. |
| [clearQuickStyleGallery()](#clearQuickStyleGallery) | يزيل جميع الأنماط من لوحة معرض الأنماط السريعة. |
| [get(int index)](#get-int) | يحصل على نمط حسب الفهرس. |
| [get(String name)](#get-java.lang.String) | يسترجع نمطًا من المجموعة. |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int) |  |
| [getCount()](#getCount) | يحصل على عدد الأنماط في المجموعة. |
| [getDefaultFont()](#getDefaultFont) | يحصل على تنسيق النص الافتراضي للمستند. |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat) | يحصل على تنسيق الفقرة الافتراضي للمستند. |
| [getDocument()](#getDocument) | يحصل على المستند المالك. |
| [iterator()](#iterator) | يحصل على كائن عداد سيقوم بترقيم الأنماط بترتيب أبجدي حسب أسمائها. |
### add(int type, String name) {#add-int-java.lang.String}
```
public Style add(int type, String name)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نوع | int |  |
| الاسم | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### addCopy(Style style) {#addCopy-com.aspose.words.Style}
```
public Style addCopy(Style style)
```


ينسخ نمطًا إلى هذه المجموعة.

 **Remarks:** 

يمكن أن يكون النمط المراد نسخه تابعًا لنفس المستند أو لمستند مختلف.

تم نسخ النمط المرتبط.

هذه الطريقة لا تنسخ الأنماط الأساسية.

إذا كانت المجموعة تحتوي بالفعل على نمط بالاسم نفسه، فسيتم إنشاء اسم جديد تلقائيًا بإضافة اللاحقة "\_number" بدءًا من 0، مثل "Normal\_0"، "Heading 1\_1" إلخ. استخدم [Style.getName()](../../com.aspose.words/style/\#getName) / [Style.setName(java.lang.String)](../../com.aspose.words/style/\#setName-java.lang.String) لتغيير اسم النمط المستورد.

 **Examples:** 

يوضح كيفية استنساخ نمط المستند.

```

 Document doc = new Document();

 // The AddCopy method creates a copy of the specified style and
 // automatically generates a new name for the style, such as "Heading 1_0".
 Style newStyle = doc.getStyles().addCopy(doc.getStyles().get("Heading 1"));

 // Use the style's "Name" property to change the style's identifying name.
 newStyle.setName("My Heading 1");

 // Our document now has two identical looking styles with different names.
 // Changing settings of one of the styles do not affect the other.
 newStyle.getFont().setColor(Color.RED);

 Assert.assertEquals("My Heading 1", newStyle.getName());
 Assert.assertEquals("Heading 1", doc.getStyles().get("Heading 1").getName());

 Assert.assertEquals(doc.getStyles().get("Heading 1").getType(), newStyle.getType());
 Assert.assertEquals(doc.getStyles().get("Heading 1").getFont().getName(), newStyle.getFont().getName());
 Assert.assertEquals(doc.getStyles().get("Heading 1").getFont().getSize(), newStyle.getFont().getSize());
 Assert.assertNotEquals(doc.getStyles().get("Heading 1").getFont().getColor(), newStyle.getFont().getColor());
 
```

يوضح كيفية استيراد نمط من مستند إلى مستند مختلف.

```

 Document srcDoc = new Document();

 // Create a custom style for the source document.
 Style srcStyle = srcDoc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 srcStyle.getFont().setColor(Color.RED);

 // Import the source document's custom style into the destination document.
 Document dstDoc = new Document();
 Style newStyle = dstDoc.getStyles().addCopy(srcStyle);

 // The imported style has an appearance identical to its source style.
 Assert.assertEquals("MyStyle", newStyle.getName());
 Assert.assertEquals(Color.RED.getRGB(), newStyle.getFont().getColor().getRGB());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) | النمط المراد نسخه. |

**Returns:**
[Style](../../com.aspose.words/style/) - Copied style ready for usage.
### clearQuickStyleGallery() {#clearQuickStyleGallery}
```
public void clearQuickStyleGallery()
```


يزيل جميع الأنماط من لوحة معرض الأنماط السريعة.

 **Examples:** 

يوضح كيفية إزالة الأنماط من لوحة معرض الأنماط.

```

 Document doc = new Document();

 // Note that remove styles work only with DOCX format for now.
 doc.getStyles().clearQuickStyleGallery();

 doc.save(getArtifactsDir() + "Styles.RemoveStylesFromStyleGallery.docx");
 
```

### get(int index) {#get-int}
```
public Style get(int index)
```


يحصل على نمط حسب الفهرس.

 **Examples:** 

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
[Style](../../com.aspose.words/style/) - A style by index.
### get(String name) {#get-java.lang.String}
```
public Style get(String name)
```


يسترجع نمطًا من المجموعة. يحصل على نمط بالاسم أو الاسم المستعار.

 **Remarks:** 

حسّاس لحالة الأحرف، يُعيد  null  إذا لم يتم العثور على النمط بالاسم المحدد.

إذا كان هذا اسمًا إنجليزيًا لنمط مدمج غير موجود بعد، يتم إنشاؤه تلقائيًا.

 **Examples:** 

يظهر متى يتم إعادة حساب تخطيط الصفحة للمستند.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/) - The corresponding [Style](../../com.aspose.words/style/) value.
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int}
```
public Style getByStyleIdentifier(int sti)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sti | int |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد الأنماط في المجموعة.

 **Examples:** 

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Returns:**
int - عدد الأنماط في المجموعة.
### getDefaultFont() {#getDefaultFont}
```
public Font getDefaultFont()
```


يحصل على تنسيق النص الافتراضي للمستند.

 **Remarks:** 

لاحظ أن الإعدادات الافتراضية على مستوى المستند تم تقديمها في Microsoft Word 2007 وتُدعم بالكامل في صيغ OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)) فقط. صيغ المستندات الأقدم تدعم هذه الميزة بشكل محدود ولا يمكن تخزين سوى أسماء الخطوط.

 **Examples:** 

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - Document default text formatting.
### getDefaultParagraphFormat() {#getDefaultParagraphFormat}
```
public ParagraphFormat getDefaultParagraphFormat()
```


يحصل على تنسيق الفقرة الافتراضي للمستند.

 **Remarks:** 

لاحظ أن الإعدادات الافتراضية على مستوى المستند تم تقديمها في Microsoft Word 2007 وتُدعم بالكامل في صيغ OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)) فقط. صيغ المستندات الأقدم لا تدعم تنسيق الفقرات الافتراضي للمستند.

 **Examples:** 

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 // Set default parameters for new styles that we may later add to this collection.
 StyleCollection styles = doc.getStyles();
 styles.getDefaultFont().setName("Courier New");

 // If we add a style of the "StyleType.Paragraph", the collection will apply the values of
 // its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
 styles.getDefaultParagraphFormat().setFirstLineIndent(15.0);

 // Add a style, and then verify that it has the default settings.
 styles.add(StyleType.PARAGRAPH, "MyStyle");

 Assert.assertEquals("Courier New", styles.get(4).getFont().getName());
 Assert.assertEquals(15.0, styles.get("MyStyle").getParagraphFormat().getFirstLineIndent());
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - Document default paragraph formatting.
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
### iterator() {#iterator}
```
public Iterator iterator()
```


يحصل على كائن عداد سيقوم بترقيم الأنماط بترتيب أبجدي حسب أسمائها.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.util.Iterator
