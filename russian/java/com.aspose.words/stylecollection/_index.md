---
title: "StyleCollection"
linktitle: "StyleCollection"
second_title: "Aspose.Words для Java"
description: "Коллекция объектов Style, представляющих как встроенные, так и пользовательские стили в документе на Java."
type: docs
weight: 642
url: /ru/java/com.aspose.words/stylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

Коллекция объектов [Style](../../com.aspose.words/style/) , представляющих как встроенные, так и пользовательские стили в документе.

Чтобы узнать больше, посетите статью документации [ Working with Styles and Themes ][Working with Styles and Themes] .

 **Examples:** 

Показывает, как создать и использовать стиль абзаца с форматированием списка.

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
## Методы

| Метод | Описание |
| --- | --- |
| [add(int type, String name)](#add-int-java.lang.String) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style) | Копирует стиль в эту коллекцию. |
| [clearQuickStyleGallery()](#clearQuickStyleGallery) | Удаляет все стили из панели Quick Style Gallery. |
| [get(int index)](#get-int) | Получает стиль по индексу. |
| [get(String name)](#get-java.lang.String) | Получает стиль из коллекции. |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int) |  |
| [getCount()](#getCount) | Получает количество стилей в коллекции. |
| [getDefaultFont()](#getDefaultFont) | Получает форматирование текста по умолчанию документа. |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat) | Получает форматирование абзаца по умолчанию документа. |
| [getDocument()](#getDocument) | Получает документ‑владельца. |
| [iterator()](#iterator) | Получает объект перечислителя, который будет перечислять стили в алфавитном порядке их имен. |
### add(int type, String name) {#add-int-java.lang.String}
```
public Style add(int type, String name)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| тип | int |  |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### addCopy(Style style) {#addCopy-com.aspose.words.Style}
```
public Style addCopy(Style style)
```


Копирует стиль в эту коллекцию.

 **Remarks:** 

Стиль, который будет копироваться, может принадлежать как тому же документу, так и другому документу.

Связанный стиль скопирован.

Этот метод не копирует базовые стили.

Если коллекция уже содержит стиль с тем же именем, то новое имя автоматически генерируется добавлением суффикса "\_number" начиная с 0, например "Normal\_0", "Heading 1\_1" и т.д. Используйте [Style.getName()](../../com.aspose.words/style/\#getName) / [Style.setName(java.lang.String)](../../com.aspose.words/style/\#setName-java.lang.String) для изменения имени импортированного стиля.

 **Examples:** 

Показывает, как клонировать стиль документа.

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

Показывает, как импортировать стиль из одного документа в другой документ.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) | Стиль для копирования. |

**Returns:**
[Style](../../com.aspose.words/style/) - Copied style ready for usage.
### clearQuickStyleGallery() {#clearQuickStyleGallery}
```
public void clearQuickStyleGallery()
```


Удаляет все стили из панели Quick Style Gallery.

 **Examples:** 

Показывает, как удалить стили из панели галереи стилей.

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


Получает стиль по индексу.

 **Examples:** 

Показывает, как добавить стиль в коллекцию стилей документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
[Style](../../com.aspose.words/style/) - A style by index.
### get(String name) {#get-java.lang.String}
```
public Style get(String name)
```


Получает стиль из коллекции.  Получает стиль по имени или псевдониму.

 **Remarks:** 

Регистрозависимый, возвращает  null  если стиль с указанным именем не найден.

Если это английское имя встроенного стиля, которого ещё не существует, он автоматически создаётся.

 **Examples:** 

Показывает, когда пересчитывать компоновку страниц документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style/) - The corresponding [Style](../../com.aspose.words/style/) value.
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int}
```
public Style getByStyleIdentifier(int sti)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sti | int |  |

**Returns:**
[Style](../../com.aspose.words/style/)
### getCount() {#getCount}
```
public int getCount()
```


Получает количество стилей в коллекции.

 **Examples:** 

Показывает, как добавить стиль в коллекцию стилей документа.

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
int - Количество стилей в коллекции.
### getDefaultFont() {#getDefaultFont}
```
public Font getDefaultFont()
```


Получает форматирование текста по умолчанию документа.

 **Remarks:** 

Обратите внимание, что настройки по умолчанию для всего документа были введены в Microsoft Word 2007 и полностью поддерживаются только в форматах OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)). Ранние форматы документов имеют ограниченную поддержку этой функции, и могут сохранять только имена шрифтов.

 **Examples:** 

Показывает, как добавить стиль в коллекцию стилей документа.

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


Получает форматирование абзаца по умолчанию документа.

 **Remarks:** 

Обратите внимание, что настройки по умолчанию для всего документа были введены в Microsoft Word 2007 и полностью поддерживаются только в форматах OOXML ( [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX)). Ранние форматы документов не поддерживают форматирование абзацев по умолчанию.

 **Examples:** 

Показывает, как добавить стиль в коллекцию стилей документа.

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


Получает документ‑владельца.

 **Examples:** 

Показывает, как получить доступ к коллекции стилей документа.

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


Получает объект перечислителя, который будет перечислять стили в алфавитном порядке их имен.

 **Examples:** 

Показывает, как получить доступ к коллекции стилей документа.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.util.Iterator
