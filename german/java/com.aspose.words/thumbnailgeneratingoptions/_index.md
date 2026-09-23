---
title: "ThumbnailGeneratingOptions"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Aspose.Words für Java"
description: "Kann verwendet werden, um zusätzliche Optionen beim Erzeugen eines Vorschaubilds für ein Dokument in Java anzugeben."
type: docs
weight: 687
url: /de/java/com.aspose.words/thumbnailgeneratingoptions/
---

**Inheritance:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

Kann verwendet werden, um zusätzliche Optionen beim Erzeugen einer Miniaturansicht für ein Dokument anzugeben.

 **Remarks:** 

Der Benutzer kann die Methode [Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document/\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) aufrufen, um [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) für ein Dokument zu erzeugen.

 **Examples:** 

Zeigt, wie man das Vorschaubild eines Dokuments aktualisiert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage) | Gibt an, ob das Vorschaubild von der ersten Seite des Dokuments oder vom ersten Bild erzeugt werden soll. |
| [getThumbnailSize()](#getThumbnailSize) | Größe des erzeugten Vorschaubilds in Pixeln. |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean) | Gibt an, ob das Vorschaubild von der ersten Seite des Dokuments oder vom ersten Bild erzeugt werden soll. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension) | Größe des erzeugten Vorschaubilds in Pixeln. |
### getGenerateFromFirstPage() {#getGenerateFromFirstPage}
```
public boolean getGenerateFromFirstPage()
```


Gibt an, ob das Vorschaubild von der ersten Seite des Dokuments oder vom ersten Bild erzeugt werden soll.

 **Remarks:** 

Standard ist  true , was bedeutet, dass das Vorschaubild von der ersten Seite des Dokuments erzeugt wird. Wenn der Wert  false  ist und kein Bild im Dokument vorhanden ist, wird das Vorschaubild von der ersten Seite des Dokuments erzeugt.

 **Examples:** 

Zeigt, wie man das Vorschaubild eines Dokuments aktualisiert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getThumbnailSize() {#getThumbnailSize}
```
public Dimension getThumbnailSize()
```


Größe des erzeugten Vorschaubilds in Pixeln. Standard ist 600x900.

 **Examples:** 

Zeigt, wie man das Vorschaubild eines Dokuments aktualisiert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Returns:**
java.awt.Dimension - Der entsprechende java.awt.Dimension-Wert.
### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean}
```
public void setGenerateFromFirstPage(boolean value)
```


Gibt an, ob das Vorschaubild von der ersten Seite des Dokuments oder vom ersten Bild erzeugt werden soll.

 **Remarks:** 

Standard ist  true , was bedeutet, dass das Vorschaubild von der ersten Seite des Dokuments erzeugt wird. Wenn der Wert  false  ist und kein Bild im Dokument vorhanden ist, wird das Vorschaubild von der ersten Seite des Dokuments erzeugt.

 **Examples:** 

Zeigt, wie man das Vorschaubild eines Dokuments aktualisiert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension}
```
public void setThumbnailSize(Dimension value)
```


Größe des erzeugten Vorschaubilds in Pixeln. Standard ist 600x900.

 **Examples:** 

Zeigt, wie man das Vorschaubild eines Dokuments aktualisiert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Dimension | Der entsprechende java.awt.Dimension-Wert. |

