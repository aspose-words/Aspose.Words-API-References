---
title: "ViewOptions"
linktitle: "ViewOptions"
second_title: "Aspose.Words für Java"
description: "Stellt verschiedene Optionen bereit, die steuern, wie ein Dokument in Microsoft Word in Java angezeigt wird."
type: docs
weight: 714
url: /de/java/com.aspose.words/viewoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ViewOptions implements Cloneable
```

Bietet verschiedene Optionen, die steuern, wie ein Dokument in Microsoft Word angezeigt wird.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Work with Options and Appearance of Word Documents ][Work with Options and Appearance of Word Documents].

 **Examples:** 

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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

Zeigt, wie man einen benutzerdefinierten Zoomtyp festlegt, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape) | Steuert die Anzeige der Hintergrundform in der Drucklayoutansicht. |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries) | Schaltet die Anzeige des Abstands zwischen dem oberen Rand des Textes und dem oberen Rand der Seite aus. |
| [getFormsDesign()](#getFormsDesign) | Gibt an, ob das Dokument im Formular-Designmodus ist. |
| [getViewType()](#getViewType) | Steuert den Ansichtsmodus in Microsoft Word. |
| [getZoomPercent()](#getZoomPercent) | Ermittelt den Prozentsatz, mit dem Sie Ihr Dokument anzeigen möchten. |
| [getZoomType()](#getZoomType) | Ermittelt einen Zoomwert basierend auf der Größe des Fensters. |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean) | Steuert die Anzeige der Hintergrundform in der Drucklayoutansicht. |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean) | Schaltet die Anzeige des Abstands zwischen dem oberen Rand des Textes und dem oberen Rand der Seite aus. |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean) | Gibt an, ob das Dokument im Formular-Designmodus ist. |
| [setViewType(int value)](#setViewType-int) | Steuert den Ansichtsmodus in Microsoft Word. |
| [setZoomPercent(int value)](#setZoomPercent-int) | Legt den Prozentsatz fest, mit dem Sie Ihr Dokument anzeigen möchten. |
| [setZoomType(int value)](#setZoomType-int) | Legt einen Zoomwert fest, basierend auf der Größe des Fensters. |
### getDisplayBackgroundShape() {#getDisplayBackgroundShape}
```
public boolean getDisplayBackgroundShape()
```


Steuert die Anzeige der Hintergrundform in der Drucklayoutansicht.

 **Examples:** 

Zeigt, wie man Dokument-Hintergrundbilder in den Ansichtoptionen ausblendet/anzeigt.

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
boolean - Der entsprechende  boolean  Wert.
### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries}
```
public boolean getDoNotDisplayPageBoundaries()
```


Schaltet die Anzeige des Abstands zwischen dem oberen Rand des Textes und dem oberen Rand der Seite aus.

 **Examples:** 

Zeigt, wie man vertikalen Leerraum und Kopf-/Fußzeilen in den Ansichtoptionen ausblendet.

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
boolean - Der entsprechende  boolean  Wert.
### getFormsDesign() {#getFormsDesign}
```
public boolean getFormsDesign()
```


Gibt an, ob das Dokument im Formular-Designmodus ist.

 **Remarks:** 

Funktioniert derzeit nur für Dokumente im WordML-Format.

 **Examples:** 

Zeigt, wie man den Formular-Designmodus aktiviert/deaktiviert.

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
boolean - Der entsprechende  boolean  Wert.
### getViewType() {#getViewType}
```
public int getViewType()
```


Steuert den Ansichtsmodus in Microsoft Word.

 **Remarks:** 

Obwohl Aspose.Words diese Option lesen und schreiben kann, ist ihre Verwendung anwendungsspezifisch. Zum Beispiel respektiert MS Word 2013 den Wert dieser Option nicht.

 **Examples:** 

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der Konstanten aus [ViewType](../../com.aspose.words/viewtype/).
### getZoomPercent() {#getZoomPercent}
```
public int getZoomPercent()
```


Ermittelt den Prozentsatz, mit dem Sie Ihr Dokument anzeigen möchten.

 **Remarks:** 

Obwohl Aspose.Words diese Option lesen und schreiben kann, ist ihre Verwendung anwendungsspezifisch. Zum Beispiel respektiert MS Word 2013 den Wert dieser Option nicht.

 **Examples:** 

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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
int - Der Prozentsatz, mit dem Sie Ihr Dokument anzeigen möchten.
### getZoomType() {#getZoomType}
```
public int getZoomType()
```


Ermittelt einen Zoomwert basierend auf der Größe des Fensters.

 **Examples:** 

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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

Zeigt, wie man einen benutzerdefinierten Zoomtyp festlegt, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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
int - Ein Zoomwert, der auf der Größe des Fensters basiert. Der zurückgegebene Wert ist einer der [ZoomType](../../com.aspose.words/zoomtype/) Konstanten.
### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean}
```
public void setDisplayBackgroundShape(boolean value)
```


Steuert die Anzeige der Hintergrundform in der Drucklayoutansicht.

 **Examples:** 

Zeigt, wie man Dokument-Hintergrundbilder in den Ansichtoptionen ausblendet/anzeigt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


Schaltet die Anzeige des Abstands zwischen dem oberen Rand des Textes und dem oberen Rand der Seite aus.

 **Examples:** 

Zeigt, wie man vertikalen Leerraum und Kopf-/Fußzeilen in den Ansichtoptionen ausblendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setFormsDesign(boolean value) {#setFormsDesign-boolean}
```
public void setFormsDesign(boolean value)
```


Gibt an, ob das Dokument im Formular-Designmodus ist.

 **Remarks:** 

Funktioniert derzeit nur für Dokumente im WordML-Format.

 **Examples:** 

Zeigt, wie man den Formular-Designmodus aktiviert/deaktiviert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setViewType(int value) {#setViewType-int}
```
public void setViewType(int value)
```


Steuert den Ansichtsmodus in Microsoft Word.

 **Remarks:** 

Obwohl Aspose.Words diese Option lesen und schreiben kann, ist ihre Verwendung anwendungsspezifisch. Zum Beispiel respektiert MS Word 2013 den Wert dieser Option nicht.

 **Examples:** 

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der [ViewType](../../com.aspose.words/viewtype/) Konstanten sein. |

### setZoomPercent(int value) {#setZoomPercent-int}
```
public void setZoomPercent(int value)
```


Legt den Prozentsatz fest, mit dem Sie Ihr Dokument anzeigen möchten.

 **Remarks:** 

Obwohl Aspose.Words diese Option lesen und schreiben kann, ist ihre Verwendung anwendungsspezifisch. Zum Beispiel respektiert MS Word 2013 den Wert dieser Option nicht.

 **Examples:** 

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Prozentsatz, mit dem Sie Ihr Dokument anzeigen möchten. |

### setZoomType(int value) {#setZoomType-int}
```
public void setZoomType(int value)
```


Legt einen Zoomwert fest, basierend auf der Größe des Fensters.

 **Examples:** 

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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

Zeigt, wie man einen benutzerdefinierten Zoomtyp festlegt, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Ein Zoomwert, der auf der Größe des Fensters basiert. Der Wert muss einer der [ZoomType](../../com.aspose.words/zoomtype/) Konstanten sein. |

