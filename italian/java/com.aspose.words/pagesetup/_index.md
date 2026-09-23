---
title: "PageSetup"
linktitle: "PageSetup"
second_title: "Aspose.Words per Java"
description: "Rappresenta le proprietà di configurazione della pagina di una sezione in Java."
type: docs
weight: 519
url: /it/java/com.aspose.words/pagesetup/
---

**Inheritance:**
java.lang.Object
```
public class PageSetup
```

Rappresenta le proprietà di configurazione della pagina di una sezione.

Per saperne di più, visita l'articolo della documentazione [ Working with Sections ][Working with Sections].

 **Remarks:** 

[PageSetup](../../com.aspose.words/pagesetup/) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

 **Examples:** 

Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Ripristina la configurazione della pagina alle dimensioni predefinite della carta, ai margini e all'orientamento. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [getBidi()](#getBidi) | Specifica che questa sezione contiene testo bidirezionale (script complessi). |
| [getBorderAlwaysInFront()](#getBorderAlwaysInFront) | Specifica dove il bordo della pagina è posizionato rispetto a testi e oggetti intersecanti. |
| [getBorderAppliesTo()](#getBorderAppliesTo) | Specifica su quali pagine il bordo della pagina viene stampato. |
| [getBorderDistanceFrom()](#getBorderDistanceFrom) | Ottiene un valore che indica se il bordo della pagina specificato è misurato dal bordo della pagina o dal testo che lo circonda. |
| [getBorderSurroundsFooter()](#getBorderSurroundsFooter) | Specifica se il bordo della pagina include o esclude il piè di pagina. |
| [getBorderSurroundsHeader()](#getBorderSurroundsHeader) | Specifica se il bordo della pagina include o esclude l'intestazione. |
| [getBorders()](#getBorders) | Ottiene una raccolta dei bordi della pagina. |
| [getBottomMargin()](#getBottomMargin) | Ottiene la distanza (in punti) tra il bordo inferiore della pagina e il limite inferiore del testo del corpo. |
| [getChapterPageSeparator()](#getChapterPageSeparator) | Ottiene il carattere separatore che appare tra il numero del capitolo e il numero della pagina. |
| [getCharactersPerLine()](#getCharactersPerLine) | Ottiene il numero di caratteri per riga nella griglia del documento. |
| [getDifferentFirstPageHeaderFooter()](#getDifferentFirstPageHeaderFooter) | Vero se un'intestazione o un piè di pagina diverso è usato nella prima pagina. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getEndnoteOptions()](#getEndnoteOptions) | Fornisce opzioni che controllano la numerazione e il posizionamento delle note finali in questa sezione. |
| [getFirstPageTray()](#getFirstPageTray) | Ottiene il vassoio (cassetto) della carta da usare per la prima pagina di una sezione. |
| [getFooterDistance()](#getFooterDistance) | Ottiene la distanza (in punti) tra il piè di pagina e il bordo inferiore della pagina. |
| [getFootnoteOptions()](#getFootnoteOptions) | Fornisce opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questa sezione. |
| [getGutter()](#getGutter) | Ottiene la quantità di spazio extra aggiunto al margine per la rilegatura del documento. |
| [getHeaderDistance()](#getHeaderDistance) | Ottiene la distanza (in punti) tra l'intestazione e il bordo superiore della pagina. |
| [getHeadingLevelForChapter()](#getHeadingLevelForChapter) | Ottiene lo stile di livello di intestazione applicato ai titoli dei capitoli nel documento. |
| [getLayoutMode()](#getLayoutMode) | Ottiene la modalità di layout di questa sezione. |
| [getLeftMargin()](#getLeftMargin) | Ottiene la distanza (in punti) tra il bordo sinistro della pagina e il limite sinistro del testo del corpo. |
| [getLineNumberCountBy()](#getLineNumberCountBy) | Ottiene l'incremento numerico per i numeri di riga. |
| [getLineNumberDistanceFromText()](#getLineNumberDistanceFromText) | Ottiene la distanza tra il bordo destro dei numeri di riga e il bordo sinistro del documento. |
| [getLineNumberRestartMode()](#getLineNumberRestartMode) | Ottiene il modo in cui viene eseguita la numerazione delle righe, cioè se ricomincia all'inizio di una nuova pagina o sezione o se continua ininterrottamente. |
| [getLineStartingNumber()](#getLineStartingNumber) | Ottiene il numero di riga iniziale. |
| [getLinesPerPage()](#getLinesPerPage) | Ottiene il numero di righe per pagina nella griglia del documento. |
| [getMargins()](#getMargins) | Ottiene i [Margini](../../com.aspose.words/margins/) predefiniti della pagina. |
| [getMultiplePages()](#getMultiplePages) | Per i documenti a più pagine, ottiene o imposta come un documento viene stampato o renderizzato in modo da poter essere rilegato come opuscolo. |
| [getOddAndEvenPagesHeaderFooter()](#getOddAndEvenPagesHeaderFooter) | True se il documento ha intestazioni e piè di pagina diversi per le pagine dispari e pari. |
| [getOrientation()](#getOrientation) | Ottiene l'orientamento della pagina. |
| [getOtherPagesTray()](#getOtherPagesTray) | Ottiene il vassoio della carta (bin) da utilizzare per tutte le pagine tranne la prima di una sezione. |
| [getPageHeight()](#getPageHeight) | Ottiene l'altezza della pagina in punti. |
| [getPageNumberStyle()](#getPageNumberStyle) | Ottiene il formato del numero di pagina. |
| [getPageStartingNumber()](#getPageStartingNumber) | Ottiene il numero di pagina iniziale della sezione. |
| [getPageWidth()](#getPageWidth) | Ottiene la larghezza della pagina in punti. |
| [getPaperSize()](#getPaperSize) | Ottiene le dimensioni della carta. |
| [getRestartPageNumbering()](#getRestartPageNumbering) | True se la numerazione delle pagine ricomincia all'inizio della sezione. |
| [getRightMargin()](#getRightMargin) | Ottiene la distanza (in punti) tra il bordo destro della pagina e il confine destro del testo del corpo. |
| [getRtlGutter()](#getRtlGutter) | Ottiene se Microsoft Word utilizza i margini interni per la sezione in base a una lingua da destra a sinistra o da sinistra a destra. |
| [getSectionStart()](#getSectionStart) | Ottiene il tipo di interruzione di sezione per l'oggetto specificato. |
| [getSheetsPerBooklet()](#getSheetsPerBooklet) | Ottiene il numero di pagine da includere in ogni opuscolo. |
| [getSuppressEndnotes()](#getSuppressEndnotes) | True se le note finali sono stampate alla fine della sezione successiva che non sopprime le note finali. |
| [getTextColumns()](#getTextColumns) | Restituisce una raccolta che rappresenta l'insieme delle colonne di testo. |
| [getTextOrientation()](#getTextOrientation) | Consente di specificare [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) per l'intera pagina. |
| [getTopMargin()](#getTopMargin) | Ottiene la distanza (in punti) tra il bordo superiore della pagina e il confine superiore del testo del corpo. |
| [getVerticalAlignment()](#getVerticalAlignment) | Ottiene l'allineamento verticale del testo su ogni pagina in un documento o sezione. |
| [setBidi(boolean value)](#setBidi-boolean) | Specifica che questa sezione contiene testo bidirezionale (script complessi). |
| [setBorderAlwaysInFront(boolean value)](#setBorderAlwaysInFront-boolean) | Specifica dove il bordo della pagina è posizionato rispetto a testi e oggetti intersecanti. |
| [setBorderAppliesTo(int value)](#setBorderAppliesTo-int) | Specifica su quali pagine il bordo della pagina viene stampato. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBorderDistanceFrom(int value)](#setBorderDistanceFrom-int) | Imposta un valore che indica se il bordo della pagina specificato è misurato dal bordo della pagina o dal testo che lo circonda. |
| [setBorderSurroundsFooter(boolean value)](#setBorderSurroundsFooter-boolean) | Specifica se il bordo della pagina include o esclude il piè di pagina. |
| [setBorderSurroundsHeader(boolean value)](#setBorderSurroundsHeader-boolean) | Specifica se il bordo della pagina include o esclude l'intestazione. |
| [setBottomMargin(double value)](#setBottomMargin-double) | Imposta la distanza (in punti) tra il bordo inferiore della pagina e il confine inferiore del testo del corpo. |
| [setChapterPageSeparator(int value)](#setChapterPageSeparator-int) | Imposta il carattere separatore che appare tra il numero del capitolo e il numero di pagina. |
| [setCharactersPerLine(int value)](#setCharactersPerLine-int) | Imposta il numero di caratteri per riga nella griglia del documento. |
| [setDifferentFirstPageHeaderFooter(boolean value)](#setDifferentFirstPageHeaderFooter-boolean) | Vero se un'intestazione o un piè di pagina diverso è usato nella prima pagina. |
| [setFirstPageTray(int value)](#setFirstPageTray-int) | Imposta il vassoio della carta (contenitore) da utilizzare per la prima pagina di una sezione. |
| [setFooterDistance(double value)](#setFooterDistance-double) | Imposta la distanza (in punti) tra il piè di pagina e il bordo inferiore della pagina. |
| [setGutter(double value)](#setGutter-double) | Imposta la quantità di spazio extra aggiunto al margine per la rilegatura del documento. |
| [setHeaderDistance(double value)](#setHeaderDistance-double) | Imposta la distanza (in punti) tra l'intestazione e la parte superiore della pagina. |
| [setHeadingLevelForChapter(int value)](#setHeadingLevelForChapter-int) | Imposta lo stile del livello di intestazione che viene applicato ai titoli dei capitoli nel documento. |
| [setLayoutMode(int value)](#setLayoutMode-int) | Imposta la modalità di layout di questa sezione. |
| [setLeftMargin(double value)](#setLeftMargin-double) | Imposta la distanza (in punti) tra il bordo sinistro della pagina e il confine sinistro del testo del corpo. |
| [setLineNumberCountBy(int value)](#setLineNumberCountBy-int) | Imposta l'incremento numerico per i numeri di riga. |
| [setLineNumberDistanceFromText(double value)](#setLineNumberDistanceFromText-double) | Imposta la distanza tra il bordo destro dei numeri di riga e il bordo sinistro del documento. |
| [setLineNumberRestartMode(int value)](#setLineNumberRestartMode-int) | Imposta il modo in cui avviene la numerazione delle righe, cioè se ricomincia all'inizio di una nuova pagina o sezione o se continua ininterrottamente. |
| [setLineStartingNumber(int value)](#setLineStartingNumber-int) | Imposta il numero di riga iniziale. |
| [setLinesPerPage(int value)](#setLinesPerPage-int) | Imposta il numero di righe per pagina nella griglia del documento. |
| [setMargins(int value)](#setMargins-int) | Imposta i [Margini](../../com.aspose.words/margins/) predefiniti della pagina. |
| [setMultiplePages(int value)](#setMultiplePages-int) | Per i documenti a più pagine, ottiene o imposta come un documento viene stampato o renderizzato in modo da poter essere rilegato come opuscolo. |
| [setOddAndEvenPagesHeaderFooter(boolean value)](#setOddAndEvenPagesHeaderFooter-boolean) | True se il documento ha intestazioni e piè di pagina diversi per le pagine dispari e pari. |
| [setOrientation(int value)](#setOrientation-int) | Imposta l'orientamento della pagina. |
| [setOtherPagesTray(int value)](#setOtherPagesTray-int) | Imposta il vassoio della carta (contenitore) da utilizzare per tutte le pagine tranne la prima di una sezione. |
| [setPageHeight(double value)](#setPageHeight-double) | Imposta l'altezza della pagina in punti. |
| [setPageNumberStyle(int value)](#setPageNumberStyle-int) | Imposta il formato del numero di pagina. |
| [setPageStartingNumber(int value)](#setPageStartingNumber-int) | Imposta il numero di pagina iniziale della sezione. |
| [setPageWidth(double value)](#setPageWidth-double) | Imposta la larghezza della pagina in punti. |
| [setPaperSize(int value)](#setPaperSize-int) | Imposta la dimensione della carta. |
| [setRestartPageNumbering(boolean value)](#setRestartPageNumbering-boolean) | True se la numerazione delle pagine ricomincia all'inizio della sezione. |
| [setRightMargin(double value)](#setRightMargin-double) | Imposta la distanza (in punti) tra il bordo destro della pagina e il confine destro del testo del corpo. |
| [setRtlGutter(boolean value)](#setRtlGutter-boolean) | Imposta se Microsoft Word utilizza i margini interni per la sezione in base a una lingua da destra a sinistra o da sinistra a destra. |
| [setSectionStart(int value)](#setSectionStart-int) | Imposta il tipo di interruzione di sezione per l'oggetto specificato. |
| [setSheetsPerBooklet(int value)](#setSheetsPerBooklet-int) | Imposta il numero di pagine da includere in ogni opuscolo. |
| [setSuppressEndnotes(boolean value)](#setSuppressEndnotes-boolean) | True se le note finali sono stampate alla fine della sezione successiva che non sopprime le note finali. |
| [setTextOrientation(int value)](#setTextOrientation-int) | Consente di specificare [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) per l'intera pagina. |
| [setTopMargin(double value)](#setTopMargin-double) | Imposta la distanza (in punti) tra il bordo superiore della pagina e il limite superiore del testo del corpo. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Imposta l'allineamento verticale del testo su ogni pagina in un documento o sezione. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Ripristina la configurazione della pagina alle dimensioni predefinite della carta, ai margini e all'orientamento.

 **Examples:** 

Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Specifica che questa sezione contiene testo bidirezionale (script complessi).

 **Remarks:** 

Quando  true , le colonne in questa sezione sono disposte da destra a sinistra.

 **Examples:** 

Mostra come impostare l'ordine delle colonne di testo in una sezione.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getTextColumns().setCount(3);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 3.");

 // Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
 // The order of the columns will match the direction of the right-to-left text.
 // Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
 // The order of the columns will match the direction of the left-to-right text.
 pageSetup.setBidi(reverseColumns);

 doc.save(getArtifactsDir() + "PageSetup.Bidi.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getBorderAlwaysInFront() {#getBorderAlwaysInFront}
```
public boolean getBorderAlwaysInFront()
```


Specifica dove il bordo della pagina è posizionato rispetto a testi e oggetti intersecanti.

 **Examples:** 

Mostra come creare un bordo a banda blu larga nella parte superiore della prima pagina.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getBorderAppliesTo() {#getBorderAppliesTo}
```
public int getBorderAppliesTo()
```


Specifica su quali pagine il bordo della pagina viene stampato.

 **Examples:** 

Mostra come creare un bordo a banda blu larga nella parte superiore della prima pagina.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
int - Il valore int corrispondente. Il valore restituito è uno dei costanti [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/).
### getBorderDistanceFrom() {#getBorderDistanceFrom}
```
public int getBorderDistanceFrom()
```


Ottiene un valore che indica se il bordo della pagina specificato è misurato dal bordo della pagina o dal testo che lo circonda.

 **Examples:** 

Mostra come creare un bordo a banda blu larga nella parte superiore della prima pagina.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
int - Un valore che indica se il bordo pagina specificato è misurato dal bordo della pagina o dal testo che lo circonda. Il valore restituito è uno dei costanti [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/).
### getBorderSurroundsFooter() {#getBorderSurroundsFooter}
```
public boolean getBorderSurroundsFooter()
```


Specifica se il bordo della pagina include o esclude il piè di pagina.

 **Remarks:** 

Nota, la modifica di questa proprietà influisce su tutte le sezioni del documento.

 **Examples:** 

Mostra come applicare un bordo alla pagina e all'intestazione/piè di pagina.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getBorderSurroundsHeader() {#getBorderSurroundsHeader}
```
public boolean getBorderSurroundsHeader()
```


Specifica se il bordo della pagina include o esclude l'intestazione.

 **Remarks:** 

Nota, la modifica di questa proprietà influisce su tutte le sezioni del documento.

 **Examples:** 

Mostra come applicare un bordo alla pagina e all'intestazione/piè di pagina.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Ottiene una raccolta dei bordi della pagina.

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - A collection of the page borders.
### getBottomMargin() {#getBottomMargin}
```
public double getBottomMargin()
```


Ottiene la distanza (in punti) tra il bordo inferiore della pagina e il limite inferiore del testo del corpo.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distanza (in punti) tra il bordo inferiore della pagina e il limite inferiore del testo del corpo.
### getChapterPageSeparator() {#getChapterPageSeparator}
```
public int getChapterPageSeparator()
```


Ottiene il carattere separatore che appare tra il numero del capitolo e il numero della pagina.

 **Remarks:** 

Prima di poter creare numeri di pagina che includono i numeri dei capitoli, le intestazioni del documento devono avere applicato un formato di struttura numerata.

 **Examples:** 

Mostra come lavorare con i capitoli di pagina.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - Il carattere separatore che appare tra il numero del capitolo e il numero di pagina. Il valore restituito è uno dei costanti [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/).
### getCharactersPerLine() {#getCharactersPerLine}
```
public int getCharactersPerLine()
```


Ottiene il numero di caratteri per riga nella griglia del documento.

 **Remarks:** 

Il valore minimo della proprietà è 1. Il valore massimo dipende dalla larghezza della pagina e dalla dimensione del carattere dello stile Normale. La spaziatura minima dei caratteri è il 90 percento della dimensione del carattere. Per esempio, il numero massimo di caratteri per riga di una pagina Letter con margini di un pollice è 43.

Per impostazione predefinita, la proprietà ha un valore in cui la spaziatura dei caratteri è uguale alla dimensione del carattere dello stile Normale.

 **Examples:** 

Mostra come specificare un valore per il numero di caratteri che ogni riga può avere.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

**Returns:**
int - Il numero di caratteri per riga nella griglia del documento.
### getDifferentFirstPageHeaderFooter() {#getDifferentFirstPageHeaderFooter}
```
public boolean getDifferentFirstPageHeaderFooter()
```


Vero se un'intestazione o un piè di pagina diverso è usato nella prima pagina.

 **Examples:** 

Mostra come creare intestazioni e piè di pagina in un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Mostra come tracciare l'ordine in cui un'operazione di sostituzione del testo attraversa i nodi.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

Mostra come abilitare o disabilitare le intestazioni/piè di pagina primari.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "First" header/footer, which appears on the first page of the section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.writeln("First page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_FIRST);
 builder.writeln("First page footer.");

 // 2 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
 // Set the "DifferentFirstPageHeaderFooter" property to "false"
 // to make the first page display the primary header/footer.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.DifferentFirstPageHeaderFooter.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getEndnoteOptions() {#getEndnoteOptions}
```
public EndnoteOptions getEndnoteOptions()
```


Fornisce opzioni che controllano la numerazione e il posizionamento delle note finali in questa sezione.

 **Examples:** 

Mostra come configurare le opzioni che influenzano le note a piè di pagina/note di chiusura in una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote reference text.");

 // Configure all footnotes in the first section to restart the numbering from 1
 // at each new page and display themselves directly beneath the text on every page.
 FootnoteOptions footnoteOptions = doc.getSections().get(0).getPageSetup().getFootnoteOptions();
 footnoteOptions.setPosition(FootnotePosition.BENEATH_TEXT);
 footnoteOptions.setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 footnoteOptions.setStartNumber(1);

 builder.write(" Hello again.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Endnote reference text.");

 // Configure all endnotes in the first section to maintain a continuous count throughout the section,
 // starting from 1. Also, set them all to appear collected at the end of the document.
 EndnoteOptions endnoteOptions = doc.getSections().get(0).getPageSetup().getEndnoteOptions();
 endnoteOptions.setPosition(EndnotePosition.END_OF_DOCUMENT);
 endnoteOptions.setRestartRule(FootnoteNumberingRule.CONTINUOUS);
 endnoteOptions.setStartNumber(1);

 doc.save(getArtifactsDir() + "PageSetup.FootnoteOptions.docx");
 
```

**Returns:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions/) - The corresponding [EndnoteOptions](../../com.aspose.words/endnoteoptions/) value.
### getFirstPageTray() {#getFirstPageTray}
```
public int getFirstPageTray()
```


Ottiene il vassoio (cassetto) di carta da utilizzare per la prima pagina di una sezione. Il valore è specifico dell'implementazione (stampante).

 **Examples:** 

Mostra come configurare la stampa utilizzando diversi vassoi della stampante per diverse dimensioni della carta.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Returns:**
int - Il vassoio (cassetto) di carta da utilizzare per la prima pagina di una sezione.
### getFooterDistance() {#getFooterDistance}
```
public double getFooterDistance()
```


Ottiene la distanza (in punti) tra il piè di pagina e il bordo inferiore della pagina.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distanza (in punti) tra il piè di pagina e il bordo inferiore della pagina.
### getFootnoteOptions() {#getFootnoteOptions}
```
public FootnoteOptions getFootnoteOptions()
```


Fornisce opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questa sezione.

 **Examples:** 

Mostra come configurare le opzioni che influenzano le note a piè di pagina/note di chiusura in una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote reference text.");

 // Configure all footnotes in the first section to restart the numbering from 1
 // at each new page and display themselves directly beneath the text on every page.
 FootnoteOptions footnoteOptions = doc.getSections().get(0).getPageSetup().getFootnoteOptions();
 footnoteOptions.setPosition(FootnotePosition.BENEATH_TEXT);
 footnoteOptions.setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 footnoteOptions.setStartNumber(1);

 builder.write(" Hello again.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Endnote reference text.");

 // Configure all endnotes in the first section to maintain a continuous count throughout the section,
 // starting from 1. Also, set them all to appear collected at the end of the document.
 EndnoteOptions endnoteOptions = doc.getSections().get(0).getPageSetup().getEndnoteOptions();
 endnoteOptions.setPosition(EndnotePosition.END_OF_DOCUMENT);
 endnoteOptions.setRestartRule(FootnoteNumberingRule.CONTINUOUS);
 endnoteOptions.setStartNumber(1);

 doc.save(getArtifactsDir() + "PageSetup.FootnoteOptions.docx");
 
```

**Returns:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions/) - The corresponding [FootnoteOptions](../../com.aspose.words/footnoteoptions/) value.
### getGutter() {#getGutter}
```
public double getGutter()
```


Ottiene la quantità di spazio extra aggiunto al margine per la rilegatura del documento.

 **Examples:** 

Mostra come impostare i margini a colonna.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Mostra come configurare un documento che può essere stampato come piega a libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
double - La quantità di spazio extra aggiunto al margine per la rilegatura del documento.
### getHeaderDistance() {#getHeaderDistance}
```
public double getHeaderDistance()
```


Ottiene la distanza (in punti) tra l'intestazione e il bordo superiore della pagina.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distanza (in punti) tra l'intestazione e la parte superiore della pagina.
### getHeadingLevelForChapter() {#getHeadingLevelForChapter}
```
public int getHeadingLevelForChapter()
```


Ottiene lo stile di livello di intestazione applicato ai titoli dei capitoli nel documento.

 **Remarks:** 

Può essere un numero da 0 a 9. 0 indica nessun numero di capitolo se applicato al numero di pagina.

Prima di poter creare numeri di pagina che includono i numeri dei capitoli, le intestazioni del documento devono avere applicato un formato di struttura numerata.

 **Examples:** 

Mostra come lavorare con i capitoli di pagina.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - Lo stile di livello di intestazione applicato ai titoli dei capitoli nel documento.
### getLayoutMode() {#getLayoutMode}
```
public int getLayoutMode()
```


Ottiene la modalità di layout di questa sezione.

 **Examples:** 

Mostra come specificare un valore per il numero di caratteri che ogni riga può avere.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Mostra come specificare un limite per il numero di righe che ogni pagina può contenere.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
int - La modalità di layout di questa sezione. Il valore restituito è una delle costanti di [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/).
### getLeftMargin() {#getLeftMargin}
```
public double getLeftMargin()
```


Ottiene la distanza (in punti) tra il bordo sinistro della pagina e il limite sinistro del testo del corpo.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distanza (in punti) tra il bordo sinistro della pagina e il limite sinistro del testo del corpo.
### getLineNumberCountBy() {#getLineNumberCountBy}
```
public int getLineNumberCountBy()
```


Ottiene l'incremento numerico per i numeri di riga.

 **Examples:** 

Mostra come abilitare la numerazione delle righe per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - L'incremento numerico per i numeri di riga.
### getLineNumberDistanceFromText() {#getLineNumberDistanceFromText}
```
public double getLineNumberDistanceFromText()
```


Ottiene la distanza tra il bordo destro dei numeri di riga e il bordo sinistro del documento.

 **Remarks:** 

Imposta questa proprietà a zero per una distanza automatica tra i numeri di riga e il testo del documento.

 **Examples:** 

Mostra come abilitare la numerazione delle righe per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
double - Distanza tra il bordo destro dei numeri di riga e il bordo sinistro del documento.
### getLineNumberRestartMode() {#getLineNumberRestartMode}
```
public int getLineNumberRestartMode()
```


Ottiene il modo in cui viene eseguita la numerazione delle righe, cioè se ricomincia all'inizio di una nuova pagina o sezione o se continua ininterrottamente.

 **Examples:** 

Mostra come abilitare la numerazione delle righe per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - Il modo in cui la numerazione delle righe viene eseguita, ovvero se ricomincia all'inizio di una nuova pagina o sezione o continua ininterrottamente. Il valore restituito è una delle costanti di [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/).
### getLineStartingNumber() {#getLineStartingNumber}
```
public int getLineStartingNumber()
```


Ottiene il numero di riga iniziale.

 **Examples:** 

Mostra come abilitare la numerazione delle righe per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - Il numero di riga iniziale.
### getLinesPerPage() {#getLinesPerPage}
```
public int getLinesPerPage()
```


Ottiene il numero di righe per pagina nella griglia del documento.

 **Remarks:** 

Il valore minimo della proprietà è 1. Il valore massimo dipende dall'altezza della pagina e dalla dimensione del carattere dello stile Normale. L'interlinea minima è il 136 percento della dimensione del carattere. Per esempio, il numero massimo di righe per pagina di una pagina Letter con margini di un pollice è 39.

Per impostazione predefinita, la proprietà ha un valore in cui l'interlinea è 1,5 volte maggiore della dimensione del carattere dello stile Normale.

 **Examples:** 

Mostra come specificare un limite per il numero di righe che ogni pagina può contenere.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
int - Il numero di righe per pagina nella griglia del documento.
### getMargins() {#getMargins}
```
public int getMargins()
```


Ottiene i [Margini](../../com.aspose.words/margins/) predefiniti della pagina.

 **Examples:** 

Mostra quando ricalcolare il layout della pagina del documento.

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

**Returns:**
int - Margini predefiniti [Margins](../../com.aspose.words/margins/) della pagina. Il valore restituito è una delle costanti di [Margins](../../com.aspose.words/margins/).
### getMultiplePages() {#getMultiplePages}
```
public int getMultiplePages()
```


Per i documenti a più pagine, ottiene o imposta come un documento viene stampato o renderizzato in modo da poter essere rilegato come opuscolo.

 **Examples:** 

Mostra come impostare i margini a colonna.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Mostra come configurare un documento che può essere stampato come piega a libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [MultiplePagesType](../../com.aspose.words/multiplepagestype/).
### getOddAndEvenPagesHeaderFooter() {#getOddAndEvenPagesHeaderFooter}
```
public boolean getOddAndEvenPagesHeaderFooter()
```


True se il documento ha intestazioni e piè di pagina diversi per le pagine dispari e pari.

 **Remarks:** 

Nota, la modifica di questa proprietà influisce su tutte le sezioni del documento.

 **Examples:** 

Mostra come creare intestazioni e piè di pagina in un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Mostra come abilitare o disabilitare le intestazioni/piè di pagina delle pagine pari.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 // 2 -  The "Even" header/footer, which appears on every even page of this section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.writeln("Even page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_EVEN);
 builder.writeln("Even page footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "OddAndEvenPagesHeaderFooter" property to "true"
 // to display the even page header/footer on even pages.
 // Set the "OddAndEvenPagesHeaderFooter" property to "false"
 // to display the primary header/footer on even pages.
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Ottiene l'orientamento della pagina.

 **Remarks:** 

Modificando [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int) scambia [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) e [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double).

 **Examples:** 

Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
int - L'orientamento della pagina. Il valore restituito è una delle costanti di [Orientation](../../com.aspose.words/orientation/).
### getOtherPagesTray() {#getOtherPagesTray}
```
public int getOtherPagesTray()
```


Restituisce il vassoio (bin) della carta da utilizzare per tutte le pagine tranne la prima di una sezione. Il valore è specifico dell'implementazione (stampante).

 **Examples:** 

Mostra come configurare la stampa utilizzando diversi vassoi della stampante per diverse dimensioni della carta.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Returns:**
int - Il vassoio (bin) della carta da utilizzare per tutte le pagine tranne la prima di una sezione.
### getPageHeight() {#getPageHeight}
```
public double getPageHeight()
```


Ottiene l'altezza della pagina in punti.

 **Examples:** 

Mostra come inserire un'immagine e usarla come filigrana.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

**Returns:**
double - L'altezza della pagina in punti.
### getPageNumberStyle() {#getPageNumberStyle}
```
public int getPageNumberStyle()
```


Ottiene il formato del numero di pagina.

 **Examples:** 

Mostra come impostare la numerazione delle pagine in una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
int - Il formato del numero di pagina. Il valore restituito è una delle costanti di [NumberStyle](../../com.aspose.words/numberstyle/) constants.
### getPageStartingNumber() {#getPageStartingNumber}
```
public int getPageStartingNumber()
```


Ottiene il numero di pagina iniziale della sezione.

 **Remarks:** 

La proprietà [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) , se impostata su false , sovrascriverà la proprietà [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) in modo che la numerazione delle pagine possa continuare dalla sezione precedente.

 **Examples:** 

Mostra come impostare la numerazione delle pagine in una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
int - Il numero di pagina iniziale della sezione.
### getPageWidth() {#getPageWidth}
```
public double getPageWidth()
```


Ottiene la larghezza della pagina in punti.

 **Examples:** 

Mostra come inserire un'immagine e usarla come filigrana.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Mostra come inserire un'immagine flottante e specificarne la posizione e le dimensioni.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
double - La larghezza della pagina in punti.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Ottiene le dimensioni della carta.

 **Remarks:** 

Impostando questa proprietà si aggiornano i valori di [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) e [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double). Impostando questo valore su [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) non si modificano i valori esistenti.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Mostra come impostare le dimensioni della pagina.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can change the current page's size to a pre-defined size
 // by using the "PaperSize" property of this section's PageSetup object.
 builder.getPageSetup().setPaperSize(PaperSize.TABLOID);

 Assert.assertEquals(792.0d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(1224.0d, builder.getPageSetup().getPageHeight());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 // Each section has its own PageSetup object. When we use a document builder to make a new section,
 // that section's PageSetup object inherits all the previous section's PageSetup object's values.
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 Assert.assertEquals(PaperSize.TABLOID, builder.getPageSetup().getPaperSize());

 builder.getPageSetup().setPaperSize(PaperSize.A5);
 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 Assert.assertEquals(419.55d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(595.30d, builder.getPageSetup().getPageHeight());

 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 // Set a custom size for this section's pages.
 builder.getPageSetup().setPageWidth(620.0);
 builder.getPageSetup().setPageHeight(480.0);

 Assert.assertEquals(PaperSize.CUSTOM, builder.getPageSetup().getPaperSize());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 doc.save(getArtifactsDir() + "PageSetup.PaperSizes.docx");
 
```

Mostra come impostare le dimensioni della carta JisB4 o JisB5.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Mostra come costruire manualmente un documento Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
int - La dimensione della carta. Il valore restituito è una delle costanti di [PaperSize](../../com.aspose.words/papersize/) constants.
### getRestartPageNumbering() {#getRestartPageNumbering}
```
public boolean getRestartPageNumbering()
```


True se la numerazione delle pagine ricomincia all'inizio della sezione.

 **Remarks:** 

Se impostata su false , la proprietà [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) sovrascriverà la proprietà [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) in modo che la numerazione delle pagine possa continuare dalla sezione precedente.

 **Examples:** 

Mostra come impostare la numerazione delle pagine in una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getRightMargin() {#getRightMargin}
```
public double getRightMargin()
```


Ottiene la distanza (in punti) tra il bordo destro della pagina e il confine destro del testo del corpo.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distanza (in punti) tra il bordo destro della pagina e il margine destro del testo del corpo.
### getRtlGutter() {#getRtlGutter}
```
public boolean getRtlGutter()
```


Ottiene se Microsoft Word utilizza i margini interni per la sezione in base a una lingua da destra a sinistra o da sinistra a destra.

 **Examples:** 

Mostra come impostare i margini a colonna.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

**Returns:**
boolean - Se Microsoft Word utilizza i margini interni per la sezione in base a una lingua da destra a sinistra o da sinistra a destra.
### getSectionStart() {#getSectionStart}
```
public int getSectionStart()
```


Ottiene il tipo di interruzione di sezione per l'oggetto specificato.

 **Examples:** 

Mostra come specificare in che modo una nuova sezione si separa da quella precedente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

Mostra come costruire manualmente un documento Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
int - Il tipo di interruzione di sezione per l'oggetto specificato. Il valore restituito è una delle costanti di [SectionStart](../../com.aspose.words/sectionstart/) constants.
### getSheetsPerBooklet() {#getSheetsPerBooklet}
```
public int getSheetsPerBooklet()
```


Ottiene il numero di pagine da includere in ogni opuscolo.

 **Examples:** 

Mostra come configurare un documento che può essere stampato come piega a libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
int - Il numero di pagine da includere in ogni libretto.
### getSuppressEndnotes() {#getSuppressEndnotes}
```
public boolean getSuppressEndnotes()
```


Vero se le note finali vengono stampate alla fine della sezione successiva che non sopprime le note finali. Le note finali sopresse vengono stampate prima delle note finali in quella sezione.

 **Examples:** 

Mostra come memorizzare le note finali alla fine di ogni sezione e modificarne le posizioni.

```

 public void suppressEndnotes() throws Exception {
     Document doc = new Document();
     doc.removeAllChildren();

     // By default, a document compiles all endnotes at its end.
     Assert.assertEquals(EndnotePosition.END_OF_DOCUMENT, doc.getEndnoteOptions().getPosition());

     // We use the "Position" property of the document's "EndnoteOptions" object
     // to collect endnotes at the end of each section instead.
     doc.getEndnoteOptions().setPosition(EndnotePosition.END_OF_SECTION);

     insertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
     insertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
     insertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

     // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
     // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
     // onto the next section.
     PageSetup pageSetup = doc.getSections().get(1).getPageSetup();
     pageSetup.setSuppressEndnotes(true);

     doc.save(getArtifactsDir() + "PageSetup.SuppressEndnotes.docx");
 }

 /// 
 /// Append a section with text and an endnote to a document.
 /// 
 private static void insertSectionWithEndnote(Document doc, String sectionBodyText, String endnoteText) {
     Section section = new Section(doc);

     doc.appendChild(section);

     Body body = new Body(doc);
     section.appendChild(body);

     Assert.assertEquals(body.getParentNode(), section);

     Paragraph para = new Paragraph(doc);
     body.appendChild(para);

     Assert.assertEquals(para.getParentNode(), body);

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.moveTo(para);
     builder.write(sectionBodyText);
     builder.insertFootnote(FootnoteType.ENDNOTE, endnoteText);
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getTextColumns() {#getTextColumns}
```
public TextColumnCollection getTextColumns()
```


Restituisce una raccolta che rappresenta l'insieme delle colonne di testo.

 **Examples:** 

Mostra come creare più colonne equamente distanziate in una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
[TextColumnCollection](../../com.aspose.words/textcolumncollection/) - A collection that represents the set of text columns.
### getTextOrientation() {#getTextOrientation}
```
public int getTextOrientation()
```


Consente di specificare [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) per l'intera pagina. Il valore predefinito è [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL)

 **Remarks:** 

Questa proprietà è supportata solo per i formati nativi di MS Word DOCX, WML, RTF e DOC.

 **Examples:** 

Mostra come impostare l'orientamento del testo.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
 // to the right so that all left-to-right text now goes top-to-bottom.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTextOrientation(TextOrientation.UPWARD);

 doc.save(getArtifactsDir() + "PageSetup.SetTextOrientation.docx");
 
```

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti di [TextOrientation](../../com.aspose.words/textorientation/) constants.
### getTopMargin() {#getTopMargin}
```
public double getTopMargin()
```


Ottiene la distanza (in punti) tra il bordo superiore della pagina e il confine superiore del testo del corpo.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distanza (in punti) tra il bordo superiore della pagina e il margine superiore del testo del corpo.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Ottiene l'allineamento verticale del testo su ogni pagina in un documento o sezione.

 **Examples:** 

Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
int - L'allineamento verticale del testo su ogni pagina in un documento o sezione. Il valore restituito è una delle costanti di [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/) constants.
### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Specifica che questa sezione contiene testo bidirezionale (script complessi).

 **Remarks:** 

Quando  true , le colonne in questa sezione sono disposte da destra a sinistra.

 **Examples:** 

Mostra come impostare l'ordine delle colonne di testo in una sezione.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getTextColumns().setCount(3);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 3.");

 // Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
 // The order of the columns will match the direction of the right-to-left text.
 // Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
 // The order of the columns will match the direction of the left-to-right text.
 pageSetup.setBidi(reverseColumns);

 doc.save(getArtifactsDir() + "PageSetup.Bidi.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setBorderAlwaysInFront(boolean value) {#setBorderAlwaysInFront-boolean}
```
public void setBorderAlwaysInFront(boolean value)
```


Specifica dove il bordo della pagina è posizionato rispetto a testi e oggetti intersecanti.

 **Examples:** 

Mostra come creare un bordo a banda blu larga nella parte superiore della prima pagina.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setBorderAppliesTo(int value) {#setBorderAppliesTo-int}
```
public void setBorderAppliesTo(int value)
```


Specifica su quali pagine il bordo della pagina viene stampato.

 **Examples:** 

Mostra come creare un bordo a banda blu larga nella parte superiore della prima pagina.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere uno dei costanti [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/) . |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| key | int |  |
| valore | java.lang.Object |  |

### setBorderDistanceFrom(int value) {#setBorderDistanceFrom-int}
```
public void setBorderDistanceFrom(int value)
```


Imposta un valore che indica se il bordo della pagina specificato è misurato dal bordo della pagina o dal testo che lo circonda.

 **Examples:** 

Mostra come creare un bordo a banda blu larga nella parte superiore della prima pagina.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Un valore che indica se il bordo di pagina specificato è misurato dal bordo della pagina o dal testo che lo circonda. Il valore deve essere uno dei costanti [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/) . |

### setBorderSurroundsFooter(boolean value) {#setBorderSurroundsFooter-boolean}
```
public void setBorderSurroundsFooter(boolean value)
```


Specifica se il bordo della pagina include o esclude il piè di pagina.

 **Remarks:** 

Nota, la modifica di questa proprietà influisce su tutte le sezioni del documento.

 **Examples:** 

Mostra come applicare un bordo alla pagina e all'intestazione/piè di pagina.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setBorderSurroundsHeader(boolean value) {#setBorderSurroundsHeader-boolean}
```
public void setBorderSurroundsHeader(boolean value)
```


Specifica se il bordo della pagina include o esclude l'intestazione.

 **Remarks:** 

Nota, la modifica di questa proprietà influisce su tutte le sezioni del documento.

 **Examples:** 

Mostra come applicare un bordo alla pagina e all'intestazione/piè di pagina.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setBottomMargin(double value) {#setBottomMargin-double}
```
public void setBottomMargin(double value)
```


Imposta la distanza (in punti) tra il bordo inferiore della pagina e il confine inferiore del testo del corpo.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La distanza (in punti) tra il bordo inferiore della pagina e il confine inferiore del testo del corpo. |

### setChapterPageSeparator(int value) {#setChapterPageSeparator-int}
```
public void setChapterPageSeparator(int value)
```


Imposta il carattere separatore che appare tra il numero del capitolo e il numero di pagina.

 **Remarks:** 

Prima di poter creare numeri di pagina che includono i numeri dei capitoli, le intestazioni del documento devono avere applicato un formato di struttura numerata.

 **Examples:** 

Mostra come lavorare con i capitoli di pagina.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il carattere separatore che appare tra il numero del capitolo e il numero di pagina. Il valore deve essere uno dei costanti [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/) . |

### setCharactersPerLine(int value) {#setCharactersPerLine-int}
```
public void setCharactersPerLine(int value)
```


Imposta il numero di caratteri per riga nella griglia del documento.

 **Remarks:** 

Il valore minimo della proprietà è 1. Il valore massimo dipende dalla larghezza della pagina e dalla dimensione del carattere dello stile Normale. La spaziatura minima dei caratteri è il 90 percento della dimensione del carattere. Per esempio, il numero massimo di caratteri per riga di una pagina Letter con margini di un pollice è 43.

Per impostazione predefinita, la proprietà ha un valore in cui la spaziatura dei caratteri è uguale alla dimensione del carattere dello stile Normale.

 **Examples:** 

Mostra come specificare un valore per il numero di caratteri che ogni riga può avere.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il numero di caratteri per riga nella griglia del documento. |

### setDifferentFirstPageHeaderFooter(boolean value) {#setDifferentFirstPageHeaderFooter-boolean}
```
public void setDifferentFirstPageHeaderFooter(boolean value)
```


Vero se un'intestazione o un piè di pagina diverso è usato nella prima pagina.

 **Examples:** 

Mostra come creare intestazioni e piè di pagina in un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Mostra come tracciare l'ordine in cui un'operazione di sostituzione del testo attraversa i nodi.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

Mostra come abilitare o disabilitare le intestazioni/piè di pagina primari.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "First" header/footer, which appears on the first page of the section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.writeln("First page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_FIRST);
 builder.writeln("First page footer.");

 // 2 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
 // Set the "DifferentFirstPageHeaderFooter" property to "false"
 // to make the first page display the primary header/footer.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.DifferentFirstPageHeaderFooter.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setFirstPageTray(int value) {#setFirstPageTray-int}
```
public void setFirstPageTray(int value)
```


Imposta il vassoio della carta (bin) da utilizzare per la prima pagina di una sezione. Il valore è specifico dell'implementazione (stampante).

 **Examples:** 

Mostra come configurare la stampa utilizzando diversi vassoi della stampante per diverse dimensioni della carta.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il vassoio della carta (bin) da utilizzare per la prima pagina di una sezione. |

### setFooterDistance(double value) {#setFooterDistance-double}
```
public void setFooterDistance(double value)
```


Imposta la distanza (in punti) tra il piè di pagina e il bordo inferiore della pagina.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La distanza (in punti) tra il piè di pagina e il bordo inferiore della pagina. |

### setGutter(double value) {#setGutter-double}
```
public void setGutter(double value)
```


Imposta la quantità di spazio extra aggiunto al margine per la rilegatura del documento.

 **Examples:** 

Mostra come impostare i margini a colonna.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Mostra come configurare un documento che può essere stampato come piega a libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La quantità di spazio extra aggiunto al margine per la rilegatura del documento. |

### setHeaderDistance(double value) {#setHeaderDistance-double}
```
public void setHeaderDistance(double value)
```


Imposta la distanza (in punti) tra l'intestazione e la parte superiore della pagina.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La distanza (in punti) tra l'intestazione e il bordo superiore della pagina. |

### setHeadingLevelForChapter(int value) {#setHeadingLevelForChapter-int}
```
public void setHeadingLevelForChapter(int value)
```


Imposta lo stile del livello di intestazione che viene applicato ai titoli dei capitoli nel documento.

 **Remarks:** 

Può essere un numero da 0 a 9. 0 indica nessun numero di capitolo se applicato al numero di pagina.

Prima di poter creare numeri di pagina che includono i numeri dei capitoli, le intestazioni del documento devono avere applicato un formato di struttura numerata.

 **Examples:** 

Mostra come lavorare con i capitoli di pagina.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Lo stile di livello intestazione applicato ai titoli dei capitoli nel documento. |

### setLayoutMode(int value) {#setLayoutMode-int}
```
public void setLayoutMode(int value)
```


Imposta la modalità di layout di questa sezione.

 **Examples:** 

Mostra come specificare un valore per il numero di caratteri che ogni riga può avere.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Mostra come specificare un limite per il numero di righe che ogni pagina può contenere.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | La modalità di layout di questa sezione. Il valore deve essere uno dei costanti [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/) . |

### setLeftMargin(double value) {#setLeftMargin-double}
```
public void setLeftMargin(double value)
```


Imposta la distanza (in punti) tra il bordo sinistro della pagina e il confine sinistro del testo del corpo.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La distanza (in punti) tra il bordo sinistro della pagina e il confine sinistro del testo del corpo. |

### setLineNumberCountBy(int value) {#setLineNumberCountBy-int}
```
public void setLineNumberCountBy(int value)
```


Imposta l'incremento numerico per i numeri di riga.

 **Examples:** 

Mostra come abilitare la numerazione delle righe per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | L'incremento numerico per i numeri di riga. |

### setLineNumberDistanceFromText(double value) {#setLineNumberDistanceFromText-double}
```
public void setLineNumberDistanceFromText(double value)
```


Imposta la distanza tra il bordo destro dei numeri di riga e il bordo sinistro del documento.

 **Remarks:** 

Imposta questa proprietà a zero per una distanza automatica tra i numeri di riga e il testo del documento.

 **Examples:** 

Mostra come abilitare la numerazione delle righe per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Distanza tra il bordo destro dei numeri di riga e il bordo sinistro del documento. |

### setLineNumberRestartMode(int value) {#setLineNumberRestartMode-int}
```
public void setLineNumberRestartMode(int value)
```


Imposta il modo in cui avviene la numerazione delle righe, cioè se ricomincia all'inizio di una nuova pagina o sezione o se continua ininterrottamente.

 **Examples:** 

Mostra come abilitare la numerazione delle righe per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il modo in cui la numerazione delle righe viene eseguita, cioè se ricomincia all'inizio di una nuova pagina o sezione o continua ininterrottamente. Il valore deve essere uno dei costanti [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/) . |

### setLineStartingNumber(int value) {#setLineStartingNumber-int}
```
public void setLineStartingNumber(int value)
```


Imposta il numero di riga iniziale.

 **Examples:** 

Mostra come abilitare la numerazione delle righe per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il numero di riga iniziale. |

### setLinesPerPage(int value) {#setLinesPerPage-int}
```
public void setLinesPerPage(int value)
```


Imposta il numero di righe per pagina nella griglia del documento.

 **Remarks:** 

Il valore minimo della proprietà è 1. Il valore massimo dipende dall'altezza della pagina e dalla dimensione del carattere dello stile Normale. L'interlinea minima è il 136 percento della dimensione del carattere. Per esempio, il numero massimo di righe per pagina di una pagina Letter con margini di un pollice è 39.

Per impostazione predefinita, la proprietà ha un valore in cui l'interlinea è 1,5 volte maggiore della dimensione del carattere dello stile Normale.

 **Examples:** 

Mostra come specificare un limite per il numero di righe che ogni pagina può contenere.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il numero di righe per pagina nella griglia del documento. |

### setMargins(int value) {#setMargins-int}
```
public void setMargins(int value)
```


Imposta i [Margini](../../com.aspose.words/margins/) predefiniti della pagina.

 **Examples:** 

Mostra quando ricalcolare il layout della pagina del documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Margini predefiniti [Margins](../../com.aspose.words/margins/) della pagina. Il valore deve essere uno dei costanti [Margins](../../com.aspose.words/margins/) . |

### setMultiplePages(int value) {#setMultiplePages-int}
```
public void setMultiplePages(int value)
```


Per i documenti a più pagine, ottiene o imposta come un documento viene stampato o renderizzato in modo da poter essere rilegato come opuscolo.

 **Examples:** 

Mostra come impostare i margini a colonna.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Mostra come configurare un documento che può essere stampato come piega a libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere uno dei costanti [MultiplePagesType](../../com.aspose.words/multiplepagestype/) . |

### setOddAndEvenPagesHeaderFooter(boolean value) {#setOddAndEvenPagesHeaderFooter-boolean}
```
public void setOddAndEvenPagesHeaderFooter(boolean value)
```


True se il documento ha intestazioni e piè di pagina diversi per le pagine dispari e pari.

 **Remarks:** 

Nota, la modifica di questa proprietà influisce su tutte le sezioni del documento.

 **Examples:** 

Mostra come creare intestazioni e piè di pagina in un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Mostra come abilitare o disabilitare le intestazioni/piè di pagina delle pagine pari.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 // 2 -  The "Even" header/footer, which appears on every even page of this section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.writeln("Even page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_EVEN);
 builder.writeln("Even page footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "OddAndEvenPagesHeaderFooter" property to "true"
 // to display the even page header/footer on even pages.
 // Set the "OddAndEvenPagesHeaderFooter" property to "false"
 // to display the primary header/footer on even pages.
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Imposta l'orientamento della pagina.

 **Remarks:** 

Modificando [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int) scambia [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) e [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double).

 **Examples:** 

Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | L'orientamento della pagina. Il valore deve essere uno dei costanti [Orientation](../../com.aspose.words/orientation/) . |

### setOtherPagesTray(int value) {#setOtherPagesTray-int}
```
public void setOtherPagesTray(int value)
```


Imposta il vassoio della carta (bin) da utilizzare per tutte le pagine tranne la prima di una sezione. Il valore è specifico dell'implementazione (stampante).

 **Examples:** 

Mostra come configurare la stampa utilizzando diversi vassoi della stampante per diverse dimensioni della carta.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il vassoio della carta (bin) da utilizzare per tutte le pagine tranne la prima di una sezione. |

### setPageHeight(double value) {#setPageHeight-double}
```
public void setPageHeight(double value)
```


Imposta l'altezza della pagina in punti.

 **Examples:** 

Mostra come inserire un'immagine e usarla come filigrana.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | L'altezza della pagina in punti. |

### setPageNumberStyle(int value) {#setPageNumberStyle-int}
```
public void setPageNumberStyle(int value)
```


Imposta il formato del numero di pagina.

 **Examples:** 

Mostra come impostare la numerazione delle pagine in una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il formato del numero di pagina. Il valore deve essere uno dei costanti [NumberStyle](../../com.aspose.words/numberstyle/) . |

### setPageStartingNumber(int value) {#setPageStartingNumber-int}
```
public void setPageStartingNumber(int value)
```


Imposta il numero di pagina iniziale della sezione.

 **Remarks:** 

La proprietà [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) , se impostata su false , sovrascriverà la proprietà [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) in modo che la numerazione delle pagine possa continuare dalla sezione precedente.

 **Examples:** 

Mostra come impostare la numerazione delle pagine in una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il numero di pagina iniziale della sezione. |

### setPageWidth(double value) {#setPageWidth-double}
```
public void setPageWidth(double value)
```


Imposta la larghezza della pagina in punti.

 **Examples:** 

Mostra come inserire un'immagine e usarla come filigrana.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Mostra come inserire un'immagine flottante e specificarne la posizione e le dimensioni.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La larghezza della pagina in punti. |

### setPaperSize(int value) {#setPaperSize-int}
```
public void setPaperSize(int value)
```


Imposta la dimensione della carta.

 **Remarks:** 

Impostando questa proprietà si aggiornano i valori di [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) e [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double). Impostando questo valore su [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) non si modificano i valori esistenti.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Mostra come impostare le dimensioni della pagina.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can change the current page's size to a pre-defined size
 // by using the "PaperSize" property of this section's PageSetup object.
 builder.getPageSetup().setPaperSize(PaperSize.TABLOID);

 Assert.assertEquals(792.0d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(1224.0d, builder.getPageSetup().getPageHeight());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 // Each section has its own PageSetup object. When we use a document builder to make a new section,
 // that section's PageSetup object inherits all the previous section's PageSetup object's values.
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 Assert.assertEquals(PaperSize.TABLOID, builder.getPageSetup().getPaperSize());

 builder.getPageSetup().setPaperSize(PaperSize.A5);
 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 Assert.assertEquals(419.55d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(595.30d, builder.getPageSetup().getPageHeight());

 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 // Set a custom size for this section's pages.
 builder.getPageSetup().setPageWidth(620.0);
 builder.getPageSetup().setPageHeight(480.0);

 Assert.assertEquals(PaperSize.CUSTOM, builder.getPageSetup().getPaperSize());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 doc.save(getArtifactsDir() + "PageSetup.PaperSizes.docx");
 
```

Mostra come impostare le dimensioni della carta JisB4 o JisB5.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Mostra come costruire manualmente un documento Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | La dimensione della carta. Il valore deve essere uno dei costanti [PaperSize](../../com.aspose.words/papersize/) . |

### setRestartPageNumbering(boolean value) {#setRestartPageNumbering-boolean}
```
public void setRestartPageNumbering(boolean value)
```


True se la numerazione delle pagine ricomincia all'inizio della sezione.

 **Remarks:** 

Se impostata su false , la proprietà [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) sovrascriverà la proprietà [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) in modo che la numerazione delle pagine possa continuare dalla sezione precedente.

 **Examples:** 

Mostra come impostare la numerazione delle pagine in una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setRightMargin(double value) {#setRightMargin-double}
```
public void setRightMargin(double value)
```


Imposta la distanza (in punti) tra il bordo destro della pagina e il confine destro del testo del corpo.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La distanza (in punti) tra il bordo destro della pagina e il confine destro del testo del corpo. |

### setRtlGutter(boolean value) {#setRtlGutter-boolean}
```
public void setRtlGutter(boolean value)
```


Imposta se Microsoft Word utilizza i margini interni per la sezione in base a una lingua da destra a sinistra o da sinistra a destra.

 **Examples:** 

Mostra come impostare i margini a colonna.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se Microsoft Word utilizza i margini per la sezione in base a una lingua da destra a sinistra o da sinistra a destra. |

### setSectionStart(int value) {#setSectionStart-int}
```
public void setSectionStart(int value)
```


Imposta il tipo di interruzione di sezione per l'oggetto specificato.

 **Examples:** 

Mostra come specificare in che modo una nuova sezione si separa da quella precedente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

Mostra come costruire manualmente un documento Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il tipo di interruzione di sezione per l'oggetto specificato. Il valore deve essere uno dei costanti [SectionStart](../../com.aspose.words/sectionstart/) . |

### setSheetsPerBooklet(int value) {#setSheetsPerBooklet-int}
```
public void setSheetsPerBooklet(int value)
```


Imposta il numero di pagine da includere in ogni opuscolo.

 **Examples:** 

Mostra come configurare un documento che può essere stampato come piega a libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il numero di pagine da includere in ogni libretto. |

### setSuppressEndnotes(boolean value) {#setSuppressEndnotes-boolean}
```
public void setSuppressEndnotes(boolean value)
```


Vero se le note finali vengono stampate alla fine della sezione successiva che non sopprime le note finali. Le note finali sopresse vengono stampate prima delle note finali in quella sezione.

 **Examples:** 

Mostra come memorizzare le note finali alla fine di ogni sezione e modificarne le posizioni.

```

 public void suppressEndnotes() throws Exception {
     Document doc = new Document();
     doc.removeAllChildren();

     // By default, a document compiles all endnotes at its end.
     Assert.assertEquals(EndnotePosition.END_OF_DOCUMENT, doc.getEndnoteOptions().getPosition());

     // We use the "Position" property of the document's "EndnoteOptions" object
     // to collect endnotes at the end of each section instead.
     doc.getEndnoteOptions().setPosition(EndnotePosition.END_OF_SECTION);

     insertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
     insertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
     insertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

     // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
     // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
     // onto the next section.
     PageSetup pageSetup = doc.getSections().get(1).getPageSetup();
     pageSetup.setSuppressEndnotes(true);

     doc.save(getArtifactsDir() + "PageSetup.SuppressEndnotes.docx");
 }

 /// 
 /// Append a section with text and an endnote to a document.
 /// 
 private static void insertSectionWithEndnote(Document doc, String sectionBodyText, String endnoteText) {
     Section section = new Section(doc);

     doc.appendChild(section);

     Body body = new Body(doc);
     section.appendChild(body);

     Assert.assertEquals(body.getParentNode(), section);

     Paragraph para = new Paragraph(doc);
     body.appendChild(para);

     Assert.assertEquals(para.getParentNode(), body);

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.moveTo(para);
     builder.write(sectionBodyText);
     builder.insertFootnote(FootnoteType.ENDNOTE, endnoteText);
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setTextOrientation(int value) {#setTextOrientation-int}
```
public void setTextOrientation(int value)
```


Consente di specificare [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) per l'intera pagina. Il valore predefinito è [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL)

 **Remarks:** 

Questa proprietà è supportata solo per i formati nativi di MS Word DOCX, WML, RTF e DOC.

 **Examples:** 

Mostra come impostare l'orientamento del testo.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
 // to the right so that all left-to-right text now goes top-to-bottom.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTextOrientation(TextOrientation.UPWARD);

 doc.save(getArtifactsDir() + "PageSetup.SetTextOrientation.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere uno dei costanti [TextOrientation](../../com.aspose.words/textorientation/) . |

### setTopMargin(double value) {#setTopMargin-double}
```
public void setTopMargin(double value)
```


Imposta la distanza (in punti) tra il bordo superiore della pagina e il limite superiore del testo del corpo.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La distanza (in punti) tra il bordo superiore della pagina e il confine superiore del testo del corpo. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Imposta l'allineamento verticale del testo su ogni pagina in un documento o sezione.

 **Examples:** 

Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | L'allineamento verticale del testo su ogni pagina in un documento o sezione. Il valore deve essere uno dei costanti [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/) . |

