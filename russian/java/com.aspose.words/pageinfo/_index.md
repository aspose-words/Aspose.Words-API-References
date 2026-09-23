---
title: "PageInfo"
linktitle: "PageInfo"
second_title: "Aspose.Words для Java"
description: "Представляет информацию о конкретной странице документа в Java."
type: docs
weight: 513
url: /ru/java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

Представляет информацию о конкретной странице документа.

Чтобы узнать больше, посетите статью документации [ Rendering ][Rendering].

 **Remarks:** 

Ширина и высота страницы, возвращаемые этим объектом, представляют "финальный" размер страницы, например, они уже повернуты в правильную ориентацию.


[Rendering]: https://docs.aspose.com/words/java/rendering/
## Методы

| Метод | Описание |
| --- | --- |
| [getColored()](#getColored) | Возвращает  true  если страница содержит цветное содержимое. |
| [getHeightInPoints()](#getHeightInPoints) | Получает высоту страницы в пунктах. |
| [getLandscape()](#getLandscape) | Возвращает  true  если ориентация страницы, указанная в документе для этой страницы, — альбомная. |
| [getPaperSize()](#getPaperSize) | Получает размер бумаги в виде перечисления. |
| [getPaperTray()](#getPaperTray) | Получает лоток (контейнер) бумаги для этой страницы, указанный в документе. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Вычисляет размер страницы в пикселях для заданного коэффициента масштабирования и разрешения. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Вычисляет размер страницы в пикселях для заданного коэффициента масштабирования и разрешения. |
| [getSizeInPoints()](#getSizeInPoints) | Получает размер страницы в пунктах. |
| [getWidthInPoints()](#getWidthInPoints) | Получает ширину страницы в пунктах. |
### getColored() {#getColored}
```
public boolean getColored()
```


Возвращает  true  если страница содержит цветное содержимое.

 **Examples:** 

Показывает, как проверить, находится ли страница в цвете или нет.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

Показывает, как фильтровать страницы в зависимости от их цвета.

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
boolean - true, если страницу следует пропустить; иначе — false. /
### getHeightInPoints() {#getHeightInPoints}
```
public float getHeightInPoints()
```


Получает высоту страницы в пунктах.

**Returns:**
float - Высота страницы в пунктах.
### getLandscape() {#getLandscape}
```
public boolean getLandscape()
```


Возвращает  true  если ориентация страницы, указанная в документе для этой страницы, — альбомная.

**Returns:**
boolean -  true, если ориентация страницы, указанная в документе для этой страницы, ландшафтная.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Получает размер бумаги в виде перечисления.

**Returns:**
int - Размер бумаги как перечисление. Возвращаемое значение является одной из констант [PaperSize](../../com.aspose.words/papersize/).
### getPaperTray() {#getPaperTray}
```
public int getPaperTray()
```


Получает лоток (корзину) бумаги для этой страницы, как указано в документе. Значение зависит от реализации (принтера).

**Returns:**
int - Лоток (корзина) бумаги для этой страницы, как указано в документе.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Вычисляет размер страницы в пикселях для заданного коэффициента масштабирования и разрешения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| масштаб | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| dpi | float | Разрешение (горизонтальное и вертикальное) для преобразования из пунктов в пиксели (точек на дюйм). |

**Returns:**
java.awt.Dimension - Размер страницы в пикселях.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Вычисляет размер страницы в пикселях для заданного коэффициента масштабирования и разрешения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| масштаб | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| horizontalDpi | float | Горизонтальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |
| verticalDpi | float | Вертикальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |

**Returns:**
java.awt.Dimension - Размер страницы в пикселях.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Получает размер страницы в пунктах.

**Returns:**
java.awt.geom.Point2D.Float - Размер страницы в пунктах.
### getWidthInPoints() {#getWidthInPoints}
```
public float getWidthInPoints()
```


Получает ширину страницы в пунктах.

**Returns:**
float - Ширина страницы в пунктах.
