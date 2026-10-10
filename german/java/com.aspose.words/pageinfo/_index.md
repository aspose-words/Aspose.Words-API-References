---
title: "PageInfo"
linktitle: "PageInfo"
second_title: "Aspose.Words für Java"
description: "Stellt Informationen über eine bestimmte Dokumentseite in Java dar."
type: docs
weight: 513
url: /de/java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

Stellt Informationen über eine bestimmte Dokumentseite dar.

Um mehr zu erfahren, besuchen Sie den [ Rendering ][Rendering] Dokumentationsartikel.

 **Remarks:** 

Die von diesem Objekt zurückgegebene Seitenbreite und -höhe stellen die "endgültige" Größe der Seite dar, z. B. sie sind bereits in die korrekte Ausrichtung gedreht.


[Rendering]: https://docs.aspose.com/words/java/rendering/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getColored()](#getColored) | Gibt  true  zurück, wenn die Seite farbigen Inhalt enthält. |
| [getHeightInPoints()](#getHeightInPoints) | Ermittelt die Höhe der Seite in Punkten. |
| [getLandscape()](#getLandscape) | Gibt  true  zurück, wenn die im Dokument für diese Seite angegebene Ausrichtung im Querformat vorliegt. |
| [getPaperSize()](#getPaperSize) | Liefert die Papiergröße als Aufzählung. |
| [getPaperTray()](#getPaperTray) | Liefert das Papierfach (Tray) für diese Seite, wie im Dokument angegeben. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Berechnet die Seitengröße in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Berechnet die Seitengröße in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [getSizeInPoints()](#getSizeInPoints) | Liefert die Seitengröße in Punkten. |
| [getWidthInPoints()](#getWidthInPoints) | Ermittelt die Breite der Seite in Punkten. |
### getColored() {#getColored}
```
public boolean getColored()
```


Gibt  true  zurück, wenn die Seite farbigen Inhalt enthält.

 **Examples:** 

Zeigt, wie geprüft wird, ob die Seite farbig ist oder nicht.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

Zeigt, wie Seiten basierend auf ihrer Farbe gefiltert werden.

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
boolean - true, wenn die Seite übersprungen werden soll; andernfalls false. /
### getHeightInPoints() {#getHeightInPoints}
```
public float getHeightInPoints()
```


Ermittelt die Höhe der Seite in Punkten.

**Returns:**
float - Die Höhe der Seite in Punkten.
### getLandscape() {#getLandscape}
```
public boolean getLandscape()
```


Gibt  true  zurück, wenn die im Dokument für diese Seite angegebene Ausrichtung im Querformat vorliegt.

**Returns:**
boolean -  true  wenn die im Dokument für diese Seite angegebene Ausrichtung im Querformat vorliegt.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Liefert die Papiergröße als Aufzählung.

**Returns:**
int - Die Papiergröße als Aufzählung. Der zurückgegebene Wert ist einer der Konstanten von [PaperSize](../../com.aspose.words/papersize/).
### getPaperTray() {#getPaperTray}
```
public int getPaperTray()
```


Liefert das Papierfach (Tray) für diese Seite, wie im Dokument angegeben. Der Wert ist implementierungs- (Drucker-) spezifisch.

**Returns:**
int - Das Papierfach (Tray) für diese Seite, wie im Dokument angegeben.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Berechnet die Seitengröße in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Maßstab | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| dpi | float | Die Auflösung (horizontal und vertikal), um von Punkten zu Pixeln (dots per inch) zu konvertieren. |

**Returns:**
java.awt.Dimension - Die Größe der Seite in Pixeln.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Berechnet die Seitengröße in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Maßstab | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| horizontalDpi | float | Die horizontale Auflösung, um von Punkten zu Pixeln (dots per inch) zu konvertieren. |
| verticalDpi | float | Die vertikale Auflösung, um von Punkten zu Pixeln (dots per inch) zu konvertieren. |

**Returns:**
java.awt.Dimension - Die Größe der Seite in Pixeln.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Liefert die Seitengröße in Punkten.

**Returns:**
java.awt.geom.Point2D.Float - Die Seitengröße in Punkten.
### getWidthInPoints() {#getWidthInPoints}
```
public float getWidthInPoints()
```


Ermittelt die Breite der Seite in Punkten.

**Returns:**
float - Die Breite der Seite in Punkten.
