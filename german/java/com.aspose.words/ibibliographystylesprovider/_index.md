---
title: "IBibliographyStylesProvider"
linktitle: "IBibliographyStylesProvider"
second_title: "Aspose.Words für Java"
description: "Implementieren Sie dieses Interface, um den Bibliografiestil für die FieldBibliography- und FieldCitation-Felder bereitzustellen, wenn sie in Java aktualisiert werden."
type: docs
weight: 753
url: /de/java/com.aspose.words/ibibliographystylesprovider/
---
```
public interface IBibliographyStylesProvider
```

Implementieren Sie dieses Interface, um den Bibliografiestil für die [FieldBibliography](../../com.aspose.words/fieldbibliography/) und [FieldCitation](../../com.aspose.words/fieldcitation/) Felder bereitzustellen, wenn sie aktualisiert werden.

 **Examples:** 

Zeigt, wie man integrierte Stile überschreibt oder eigene bereitstellt.

```

 public void changeBibliographyStyles() throws Exception
 {
     Document doc = new Document(getMyDir() + "Bibliography.docx");

     // If the document already has a style you can change it with the following code:
     // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

     doc.getFieldOptions().setBibliographyStylesProvider(new BibliographyStylesProvider());
     doc.updateFields();

     doc.save(getArtifactsDir() + "Field.ChangeBibliographyStyles.docx");
 }

 public static class BibliographyStylesProvider implements IBibliographyStylesProvider
 {
     public FileInputStream getStyle(String styleFileName) throws Exception
     {
         return new FileInputStream(getMyDir() + "Bibliography custom style.xsl");
     }
 }
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getStyle(String styleFileName)](#getStyle-java.lang.String) | Gibt den Bibliografiestil zurück. |
### getStyle(String styleFileName) {#getStyle-java.lang.String}
```
public abstract InputStream getStyle(String styleFileName)
```


Gibt den Bibliografiestil zurück.

 **Remarks:** 

Die Implementierung sollte  null  zurückgeben, um anzuzeigen, dass die MS‑Word‑Version des angegebenen Stils verwendet werden soll.

 **Examples:** 

Zeigt, wie man integrierte Stile überschreibt oder eigene bereitstellt.

```

 public void changeBibliographyStyles() throws Exception
 {
     Document doc = new Document(getMyDir() + "Bibliography.docx");

     // If the document already has a style you can change it with the following code:
     // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

     doc.getFieldOptions().setBibliographyStylesProvider(new BibliographyStylesProvider());
     doc.updateFields();

     doc.save(getArtifactsDir() + "Field.ChangeBibliographyStyles.docx");
 }

 public static class BibliographyStylesProvider implements IBibliographyStylesProvider
 {
     public FileInputStream getStyle(String styleFileName) throws Exception
     {
         return new FileInputStream(getMyDir() + "Bibliography custom style.xsl");
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| styleFileName | java.lang.String | Der Dateiname der Bibliografiestildatei. |

**Returns:**
java.io.InputStream - Der java.io.InputStream mit dem XSLT-Stylesheet für den Bibliografiestil.
