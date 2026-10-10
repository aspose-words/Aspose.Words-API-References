---
title: "PageInfo"
linktitle: "PageInfo"
second_title: "Aspose.Words Java için"
description: "Java'da belirli bir belge sayfası hakkında bilgi temsil eder."
type: docs
weight: 513
url: /tr/java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

Belirli bir belge sayfası hakkında bilgi temsil eder.

Daha fazla bilgi için, [ Rendering ][Rendering] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu nesne tarafından döndürülen sayfa genişliği ve yüksekliği, sayfanın "final" boyutunu temsil eder; örneğin zaten doğru yönlendirmeye göre döndürülmüşlerdir.


[Rendering]: https://docs.aspose.com/words/java/rendering/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getColored()](#getColored) | Sayfa renkli içerik içeriyorsa  true  değerini döndürür. |
| [getHeightInPoints()](#getHeightInPoints) | Sayfanın yüksekliğini puan cinsinden alır. |
| [getLandscape()](#getLandscape) | Belgedeki bu sayfa için belirtilen sayfa yönelimi yatay ise  true  değerini döndürür. |
| [getPaperSize()](#getPaperSize) | Kağıt boyutunu enum olarak alır. |
| [getPaperTray()](#getPaperTray) | Belgede belirtildiği gibi bu sayfa için kağıt tepsisini (bin) alır. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar. |
| [getSizeInPoints()](#getSizeInPoints) | Sayfa boyutunu puan cinsinden alır. |
| [getWidthInPoints()](#getWidthInPoints) | Sayfanın genişliğini puan cinsinden alır. |
### getColored() {#getColored}
```
public boolean getColored()
```


Sayfa renkli içerik içeriyorsa  true  değerini döndürür.

 **Examples:** 

Sayfanın renkli olup olmadığını nasıl kontrol edeceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

Sayfaları sayfa rengine göre nasıl filtreleyeceğinizi gösterir.

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
boolean - sayfa atlanmalıysa true; aksi takdirde false. /
### getHeightInPoints() {#getHeightInPoints}
```
public float getHeightInPoints()
```


Sayfanın yüksekliğini puan cinsinden alır.

**Returns:**
float - sayfanın yüksekliği puan cinsinden.
### getLandscape() {#getLandscape}
```
public boolean getLandscape()
```


Belgedeki bu sayfa için belirtilen sayfa yönelimi yatay ise  true  değerini döndürür.

**Returns:**
boolean - sayfa için belgede belirtilen yönlendirme yataysa true.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Kağıt boyutunu enum olarak alır.

**Returns:**
int - Kağıt boyutu bir enum olarak. Döndürülen değer [PaperSize](../../com.aspose.words/papersize/) sabitlerinden biridir.
### getPaperTray() {#getPaperTray}
```
public int getPaperTray()
```


Belgede belirtildiği gibi bu sayfa için kağıt tepsisini (bin) alır. Değer uygulamaya (yazıcıya) özgüdür.

**Returns:**
int - Belgede belirtildiği gibi bu sayfa için kağıt tepsisi (bin).
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ölçek | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| dpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için çözünürlük (yatay ve dikey). |

**Returns:**
java.awt.Dimension - sayfanın piksel cinsinden boyutu.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ölçek | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| horizontalDpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için yatay çözünürlük. |
| verticalDpi | float | Noktalardan piksellere (inç başına nokta) dönüştürmek için dikey çözünürlük. |

**Returns:**
java.awt.Dimension - sayfanın piksel cinsinden boyutu.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Sayfa boyutunu puan cinsinden alır.

**Returns:**
java.awt.geom.Point2D.Float - sayfa boyutu puan cinsinden.
### getWidthInPoints() {#getWidthInPoints}
```
public float getWidthInPoints()
```


Sayfanın genişliğini puan cinsinden alır.

**Returns:**
float - sayfanın genişliği puan cinsinden.
