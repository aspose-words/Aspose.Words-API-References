---
title: "PageInfo"
linktitle: "PageInfo"
second_title: "Aspose.Words pour Java"
description: "Représente les informations concernant une page de document particulière en Java."
type: docs
weight: 513
url: /fr/java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

Représente les informations concernant une page de document particulière.

Pour en savoir plus, consultez l'article de documentation [ Rendering ][Rendering].

 **Remarks:** 

La largeur et la hauteur de page renvoyées par cet objet représentent la taille "finale" de la page, par exemple elles sont déjà pivotées à la bonne orientation.


[Rendering]: https://docs.aspose.com/words/java/rendering/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getColored()](#getColored) | Renvoie  true  si la page contient du contenu en couleur. |
| [getHeightInPoints()](#getHeightInPoints) | Obtient la hauteur de la page en points. |
| [getLandscape()](#getLandscape) | Renvoie  true  si l'orientation de la page spécifiée dans le document pour cette page est paysage. |
| [getPaperSize()](#getPaperSize) | Obtient la taille du papier sous forme d'énumération. |
| [getPaperTray()](#getPaperTray) | Obtient le bac à papier (trémie) pour cette page tel que spécifié dans le document. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés. |
| [getSizeInPoints()](#getSizeInPoints) | Obtient la taille de la page en points. |
| [getWidthInPoints()](#getWidthInPoints) | Obtient la largeur de la page en points. |
### getColored() {#getColored}
```
public boolean getColored()
```


Renvoie  true  si la page contient du contenu en couleur.

 **Examples:** 

Montre comment vérifier si la page est en couleur ou non.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

Montre comment filtrer les pages en fonction de la couleur de la page.

```
{@code
 public void colorMode() throws Exception
 {
     // Load the document with 3 color pages and 2 black and white pages.
     Document doc = new Document("Colored pages.docx");

     // Print color pages to 'color' printer.
     int colorPagesPrinted = printPages(doc, "Microsoft Print to PDF", true);

     // Print black-and-white pages to 'black-and-white' printer.
     int nonColorPagesPrinted = printPages(doc, "Microsoft XPS Document Writer", false);

     // Verify that correct number of pages were printed in each case.
     Assert.assertEquals(3, colorPagesPrinted);
     Assert.assertEquals(3, nonColorPagesPrinted);
 }

 /// 
 /// Prints document pages filtered by color requirements.
 /// 
 /// The document to print.
 /// The name of the target printer.
 /// 
 /// true to print only color pages;
 /// false to print only black and white pages.
 /// 
 /// The number of pages actually printed.
 private int printPages(Document doc, String printerName, boolean colored) throws Exception
 {
     // Configure printer settings.
     PrinterJob printerJob = PrinterJob.getPrinterJob();

     // Select target printer.
     for (PrintService service : PrinterJob.lookupPrintServices()) {
         if (service.getName().equalsIgnoreCase(printerName)) {
             printerJob.setPrintService(service);
             break;
         }
     }

     // Create print document with color mode set to Normal.
     AsposeWordsPrintDocument printDoc = new AsposeWordsPrintDocument(doc);
     printDoc.setColorMode(ColorPrintMode.NORMAL);

     // Filter pages: skip color pages when printing black and white, and vice versa.
     printDoc.setPageIndexFilter(new ColorPagesFilter(doc, !colored));

     printerJob.setPrintable(printDoc);
     printerJob.print();

     return printDoc.getTotalPagesPrinted();
 }

 /// 
 /// A filter that selectively skips color or black-and-white pages during printing
 /// based on the document's page information and specified filtering mode.
 /// 
 /// 
 /// This filter implements the IIndexFilter interface to provide custom page selection
 /// logic for printing operations. It can be configured to either skip color pages
 /// (when printing only black-and-white content) or skip black-and-white pages
 /// (when printing only color content).
 /// 
 static class ColorPagesFilter implements IIndexFilter
 {
     private final Document doc;
     private final boolean skipColorPages;

     /**
 Initializes a new instance of the ColorPagesFilter class.
```

**Returns:**
booléen - vrai si la page doit être ignorée ; sinon, faux. /
### getHeightInPoints() {#getHeightInPoints}
```
public float getHeightInPoints()
```


Obtient la hauteur de la page en points.

**Returns:**
float - La hauteur de la page en points.
### getLandscape() {#getLandscape}
```
public boolean getLandscape()
```


Renvoie  true  si l'orientation de la page spécifiée dans le document pour cette page est paysage.

**Returns:**
booléen -  vrai  si l'orientation de la page spécifiée dans le document pour cette page est paysage.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Obtient la taille du papier sous forme d'énumération.

**Returns:**
int - La taille du papier en tant qu'énumération. La valeur retournée est l'une des constantes [PaperSize](../../com.aspose.words/papersize/).
### getPaperTray() {#getPaperTray}
```
public int getPaperTray()
```


Obtient le bac à papier (tray) pour cette page tel que spécifié dans le document. La valeur dépend de l'implémentation (imprimante).

**Returns:**
int - Le bac à papier (tray) pour cette page tel que spécifié dans le document.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| échelle | float | Le facteur de zoom (1,0 correspond à 100 %). |
| dpi | float | La résolution (horizontale et verticale) pour convertir des points en pixels (points par pouce). |

**Returns:**
java.awt.Dimension - La taille de la page en pixels.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| échelle | float | Le facteur de zoom (1,0 correspond à 100 %). |
| horizontalDpi | float | La résolution horizontale pour convertir des points en pixels (points par pouce). |
| verticalDpi | float | La résolution verticale pour convertir des points en pixels (points par pouce). |

**Returns:**
java.awt.Dimension - La taille de la page en pixels.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Obtient la taille de la page en points.

**Returns:**
java.awt.geom.Point2D.Float - La taille de la page en points.
### getWidthInPoints() {#getWidthInPoints}
```
public float getWidthInPoints()
```


Obtient la largeur de la page en points.

**Returns:**
float - La largeur de la page en points.
