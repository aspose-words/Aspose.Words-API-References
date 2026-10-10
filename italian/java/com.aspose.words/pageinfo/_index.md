---
title: "PageInfo"
linktitle: "PageInfo"
second_title: "Aspose.Words per Java"
description: "Rappresenta le informazioni su una pagina specifica di un documento in Java."
type: docs
weight: 513
url: /it/java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

Rappresenta informazioni su una specifica pagina del documento.

Per saperne di più, visita l'articolo di documentazione [ Rendering ][Rendering].

 **Remarks:** 

La larghezza e l'altezza della pagina restituite da questo oggetto rappresentano la dimensione \"finale\" della pagina, ad esempio sono già ruotate all'orientamento corretto.


[Rendering]: https://docs.aspose.com/words/java/rendering/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getColored()](#getColored) | Restituisce  true  se la pagina contiene contenuti a colori. |
| [getHeightInPoints()](#getHeightInPoints) | Ottiene l'altezza della pagina in punti. |
| [getLandscape()](#getLandscape) | Restituisce  true  se l'orientamento della pagina specificato nel documento per questa pagina è orizzontale. |
| [getPaperSize()](#getPaperSize) | Ottiene la dimensione della carta come enumerazione. |
| [getPaperTray()](#getPaperTray) | Ottiene il vassoio della carta (cassetto) per questa pagina come specificato nel documento. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Calcola la dimensione della pagina in pixel per un fattore di zoom e una risoluzione specificati. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Calcola la dimensione della pagina in pixel per un fattore di zoom e una risoluzione specificati. |
| [getSizeInPoints()](#getSizeInPoints) | Ottiene la dimensione della pagina in punti. |
| [getWidthInPoints()](#getWidthInPoints) | Ottiene la larghezza della pagina in punti. |
### getColored() {#getColored}
```
public boolean getColored()
```


Restituisce  true  se la pagina contiene contenuti a colori.

 **Examples:** 

Mostra come verificare se la pagina è a colori o meno.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

Mostra come filtrare le pagine in base al colore della pagina.

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
boolean - true se la pagina deve essere saltata; altrimenti, false. /
### getHeightInPoints() {#getHeightInPoints}
```
public float getHeightInPoints()
```


Ottiene l'altezza della pagina in punti.

**Returns:**
float - L'altezza della pagina in punti.
### getLandscape() {#getLandscape}
```
public boolean getLandscape()
```


Restituisce  true  se l'orientamento della pagina specificato nel documento per questa pagina è orizzontale.

**Returns:**
boolean -  true  se l'orientamento della pagina specificato nel documento per questa pagina è orizzontale.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Ottiene la dimensione della carta come enumerazione.

**Returns:**
int - La dimensione della carta come enumerazione. Il valore restituito è una delle costanti [PaperSize](../../com.aspose.words/papersize/).
### getPaperTray() {#getPaperTray}
```
public int getPaperTray()
```


Ottiene il vassoio della carta (bin) per questa pagina come specificato nel documento. Il valore è specifico dell'implementazione (stampante).

**Returns:**
int - Il vassoio della carta (bin) per questa pagina come specificato nel documento.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Calcola la dimensione della pagina in pixel per un fattore di zoom e una risoluzione specificati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scala | float | Il fattore di zoom (1.0 è 100%). |
| dpi | float | La risoluzione (orizzontale e verticale) per convertire da punti a pixel (punti per pollice). |

**Returns:**
java.awt.Dimension - La dimensione della pagina in pixel.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calcola la dimensione della pagina in pixel per un fattore di zoom e una risoluzione specificati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scala | float | Il fattore di zoom (1.0 è 100%). |
| horizontalDpi | float | La risoluzione orizzontale per convertire da punti a pixel (punti per pollice). |
| verticalDpi | float | La risoluzione verticale per convertire da punti a pixel (punti per pollice). |

**Returns:**
java.awt.Dimension - La dimensione della pagina in pixel.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Ottiene la dimensione della pagina in punti.

**Returns:**
java.awt.geom.Point2D.Float - La dimensione della pagina in punti.
### getWidthInPoints() {#getWidthInPoints}
```
public float getWidthInPoints()
```


Ottiene la larghezza della pagina in punti.

**Returns:**
float - La larghezza della pagina in punti.
