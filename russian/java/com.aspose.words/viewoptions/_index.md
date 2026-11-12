---
title: "ViewOptions"
linktitle: "ViewOptions"
second_title: "Aspose.Words для Java"
description: "Предоставляет различные параметры, которые управляют тем, как документ отображается в Microsoft Word на Java."
type: docs
weight: 714
url: /ru/java/com.aspose.words/viewoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ViewOptions implements Cloneable
```

Предоставляет различные параметры, контролирующие отображение документа в Microsoft Word.

Чтобы узнать больше, посетите статью документации [ Work with Options and Appearance of Word Documents ][Work with Options and Appearance of Word Documents].

 **Examples:** 

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word применяют к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Показывает, как установить пользовательский тип масштабирования, который более старые версии Microsoft Word применят к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```


[Work with Options and Appearance of Word Documents]: https://docs.aspose.com/words/java/work-with-word-document-options-and-appearance/
## Методы

| Метод | Описание |
| --- | --- |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape) | Управляет отображением фоновой формы в режиме разметки печати. |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries) | Отключает отображение пространства между верхом текста и верхним краем страницы. |
| [getFormsDesign()](#getFormsDesign) | Указывает, находится ли документ в режиме разработки форм. |
| [getViewType()](#getViewType) | Управляет режимом просмотра в Microsoft Word. |
| [getZoomPercent()](#getZoomPercent) | Получает процент, с которым вы хотите просматривать документ. |
| [getZoomType()](#getZoomType) | Получает значение масштабирования, основанное на размере окна. |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean) | Управляет отображением фоновой формы в режиме разметки печати. |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean) | Отключает отображение пространства между верхом текста и верхним краем страницы. |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean) | Указывает, находится ли документ в режиме разработки форм. |
| [setViewType(int value)](#setViewType-int) | Управляет режимом просмотра в Microsoft Word. |
| [setZoomPercent(int value)](#setZoomPercent-int) | Устанавливает процент, с которым вы хотите просматривать документ. |
| [setZoomType(int value)](#setZoomType-int) | Устанавливает значение масштабирования, основанное на размере окна. |
### getDisplayBackgroundShape() {#getDisplayBackgroundShape}
```
public boolean getDisplayBackgroundShape()
```


Управляет отображением фоновой формы в режиме разметки печати.

 **Examples:** 

Показывает, как скрыть/отобразить фоновые изображения документа в параметрах просмотра.

```

 // Use an HTML string to create a new document with a flat background color.
 final String HTML =
         "\r\n                \r\n                    Hello world!\r\n                \r\n            ";

 Document doc = new Document(new ByteArrayInputStream(HTML.getBytes()));

 // The source for the document has a flat color background,
 // the presence of which will set the "DisplayBackgroundShape" flag to "true".
 Assert.assertTrue(doc.getViewOptions().getDisplayBackgroundShape());

 // Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
 // This may affect some text colors to improve visibility.
 // Set the "DisplayBackgroundShape" to "false" to not display the background color.
 doc.getViewOptions().setDisplayBackgroundShape(displayBackgroundShape);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayBackgroundShape.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries}
```
public boolean getDoNotDisplayPageBoundaries()
```


Отключает отображение пространства между верхом текста и верхним краем страницы.

 **Examples:** 

Показывает, как скрыть вертикальные пробелы и колонтитулы в параметрах просмотра.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert content that spans across 3 pages.
 builder.writeln("Paragraph 1, Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 2, Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 3, Page 3.");

 // Insert a header and a footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("This is the footer.");

 // This document contains a small amount of content that takes up a few full pages worth of space.
 // Set the "DoNotDisplayPageBoundaries" flag to "true" to get older versions of Microsoft Word to omit headers,
 // footers, and much of the vertical whitespace when displaying our document.
 // Set the "DoNotDisplayPageBoundaries" flag to "false" to get older versions of Microsoft Word
 // to normally display our document.
 doc.getViewOptions().setDoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayPageBoundaries.doc");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getFormsDesign() {#getFormsDesign}
```
public boolean getFormsDesign()
```


Указывает, находится ли документ в режиме разработки форм.

 **Remarks:** 

В настоящее время работает только с документами в формате WordML.

 **Examples:** 

Показывает, как включить/отключить режим разработки форм.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "FormsDesign" property to "false" to keep forms design mode disabled.
 // Set the "FormsDesign" property to "true" to enable forms design mode.
 doc.getViewOptions().setFormsDesign(useFormsDesign);

 doc.save(getArtifactsDir() + "ViewOptions.FormsDesign.xml");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getViewType() {#getViewType}
```
public int getViewType()
```


Управляет режимом просмотра в Microsoft Word.

 **Remarks:** 

Хотя Aspose.Words может читать и записывать эту опцию, её использование зависит от приложения. Например, MS Word 2013 не учитывает значение этой опции.

 **Examples:** 

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word применяют к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Returns:**
int — соответствующее значение int. Возвращаемое значение является одной из констант [ViewType](../../com.aspose.words/viewtype/).
### getZoomPercent() {#getZoomPercent}
```
public int getZoomPercent()
```


Получает процент, с которым вы хотите просматривать документ.

 **Remarks:** 

Хотя Aspose.Words может читать и записывать эту опцию, её использование зависит от приложения. Например, MS Word 2013 не учитывает значение этой опции.

 **Examples:** 

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word применяют к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Returns:**
int — процент, с которым вы хотите просматривать документ.
### getZoomType() {#getZoomType}
```
public int getZoomType()
```


Получает значение масштабирования, основанное на размере окна.

 **Examples:** 

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word применяют к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Показывает, как установить пользовательский тип масштабирования, который более старые версии Microsoft Word применят к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```

**Returns:**
int — значение масштабирования, основанное на размере окна. Возвращаемое значение является одной из констант [ZoomType](../../com.aspose.words/zoomtype/).
### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean}
```
public void setDisplayBackgroundShape(boolean value)
```


Управляет отображением фоновой формы в режиме разметки печати.

 **Examples:** 

Показывает, как скрыть/отобразить фоновые изображения документа в параметрах просмотра.

```

 // Use an HTML string to create a new document with a flat background color.
 final String HTML =
         "\r\n                \r\n                    Hello world!\r\n                \r\n            ";

 Document doc = new Document(new ByteArrayInputStream(HTML.getBytes()));

 // The source for the document has a flat color background,
 // the presence of which will set the "DisplayBackgroundShape" flag to "true".
 Assert.assertTrue(doc.getViewOptions().getDisplayBackgroundShape());

 // Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
 // This may affect some text colors to improve visibility.
 // Set the "DisplayBackgroundShape" to "false" to not display the background color.
 doc.getViewOptions().setDisplayBackgroundShape(displayBackgroundShape);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayBackgroundShape.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


Отключает отображение пространства между верхом текста и верхним краем страницы.

 **Examples:** 

Показывает, как скрыть вертикальные пробелы и колонтитулы в параметрах просмотра.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert content that spans across 3 pages.
 builder.writeln("Paragraph 1, Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 2, Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 3, Page 3.");

 // Insert a header and a footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("This is the footer.");

 // This document contains a small amount of content that takes up a few full pages worth of space.
 // Set the "DoNotDisplayPageBoundaries" flag to "true" to get older versions of Microsoft Word to omit headers,
 // footers, and much of the vertical whitespace when displaying our document.
 // Set the "DoNotDisplayPageBoundaries" flag to "false" to get older versions of Microsoft Word
 // to normally display our document.
 doc.getViewOptions().setDoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayPageBoundaries.doc");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setFormsDesign(boolean value) {#setFormsDesign-boolean}
```
public void setFormsDesign(boolean value)
```


Указывает, находится ли документ в режиме разработки форм.

 **Remarks:** 

В настоящее время работает только с документами в формате WordML.

 **Examples:** 

Показывает, как включить/отключить режим разработки форм.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "FormsDesign" property to "false" to keep forms design mode disabled.
 // Set the "FormsDesign" property to "true" to enable forms design mode.
 doc.getViewOptions().setFormsDesign(useFormsDesign);

 doc.save(getArtifactsDir() + "ViewOptions.FormsDesign.xml");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setViewType(int value) {#setViewType-int}
```
public void setViewType(int value)
```


Управляет режимом просмотра в Microsoft Word.

 **Remarks:** 

Хотя Aspose.Words может читать и записывать эту опцию, её использование зависит от приложения. Например, MS Word 2013 не учитывает значение этой опции.

 **Examples:** 

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word применяют к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее значение int. Значение должно быть одной из констант [ViewType](../../com.aspose.words/viewtype/). |

### setZoomPercent(int value) {#setZoomPercent-int}
```
public void setZoomPercent(int value)
```


Устанавливает процент, с которым вы хотите просматривать документ.

 **Remarks:** 

Хотя Aspose.Words может читать и записывать эту опцию, её использование зависит от приложения. Например, MS Word 2013 не учитывает значение этой опции.

 **Examples:** 

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word применяют к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Процент, с которым вы хотите просматривать документ. |

### setZoomType(int value) {#setZoomType-int}
```
public void setZoomType(int value)
```


Устанавливает значение масштабирования, основанное на размере окна.

 **Examples:** 

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word применяют к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Показывает, как установить пользовательский тип масштабирования, который более старые версии Microsoft Word применят к документу при загрузке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение масштабирования, основанное на размере окна. Значение должно быть одной из констант [ZoomType](../../com.aspose.words/zoomtype/). |

