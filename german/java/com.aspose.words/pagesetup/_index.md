---
title: "PageSetup"
linktitle: "PageSetup"
second_title: "Aspose.Words für Java"
description: "Stellt die Seiteneinrichtungs‑Eigenschaften eines Abschnitts in Java dar."
type: docs
weight: 519
url: /de/java/com.aspose.words/pagesetup/
---

**Inheritance:**
java.lang.Object
```
public class PageSetup
```

Stellt die Seiteneinrichtungseigenschaften eines Abschnitts dar.

Um mehr zu erfahren, besuchen Sie den [ Working with Sections ][Working with Sections] Dokumentationsartikel.

 **Remarks:** 

[PageSetup](../../com.aspose.words/pagesetup/) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

 **Examples:** 

Zeigt, wie man Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument anwendet und zurücksetzt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Setzt die Seiteneinrichtung auf die Standard‑Papiergröße, Ränder und Ausrichtung zurück. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [getBidi()](#getBidi) | Gibt an, dass dieser Abschnitt bidirektionalen (komplexen Skript‑) Text enthält. |
| [getBorderAlwaysInFront()](#getBorderAlwaysInFront) | Gibt an, wo der Seitenrand relativ zu sich kreuzenden Texten und Objekten positioniert ist. |
| [getBorderAppliesTo()](#getBorderAppliesTo) | Gibt an, auf welchen Seiten der Seitenrand gedruckt wird. |
| [getBorderDistanceFrom()](#getBorderDistanceFrom) | Gibt einen Wert zurück, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umschlossenen Text gemessen wird. |
| [getBorderSurroundsFooter()](#getBorderSurroundsFooter) | Gibt an, ob der Seitenrand die Fußzeile ein- oder ausschließt. |
| [getBorderSurroundsHeader()](#getBorderSurroundsHeader) | Gibt an, ob der Seitenrand die Kopfzeile ein- oder ausschließt. |
| [getBorders()](#getBorders) | Gibt eine Sammlung der Seitenränder zurück. |
| [getBottomMargin()](#getBottomMargin) | Gibt den Abstand (in Punkten) zwischen dem unteren Rand der Seite und der unteren Begrenzung des Fließtextes zurück. |
| [getChapterPageSeparator()](#getChapterPageSeparator) | Gibt das Trennzeichen zurück, das zwischen Kapitelnummer und Seitenzahl erscheint. |
| [getCharactersPerLine()](#getCharactersPerLine) | Gibt die Anzahl der Zeichen pro Zeile im Dokumentgitter zurück. |
| [getDifferentFirstPageHeaderFooter()](#getDifferentFirstPageHeaderFooter) | Wahr, wenn auf der ersten Seite eine andere Kopf‑ oder Fußzeile verwendet wird. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getEndnoteOptions()](#getEndnoteOptions) | Bietet Optionen, die die Nummerierung und Positionierung von Endnoten in diesem Abschnitt steuern. |
| [getFirstPageTray()](#getFirstPageTray) | Gibt das Papierfach (Bin), das für die erste Seite eines Abschnitts verwendet wird, zurück. |
| [getFooterDistance()](#getFooterDistance) | Gibt den Abstand (in Punkten) zwischen der Fußzeile und dem unteren Rand der Seite zurück. |
| [getFootnoteOptions()](#getFootnoteOptions) | Bietet Optionen, die die Nummerierung und Positionierung von Fußnoten in diesem Abschnitt steuern. |
| [getGutter()](#getGutter) | Gibt die Menge des zusätzlichen Raums zurück, der dem Rand für die Dokumentbindung hinzugefügt wird. |
| [getHeaderDistance()](#getHeaderDistance) | Gibt den Abstand (in Punkten) zwischen der Kopfzeile und dem oberen Rand der Seite zurück. |
| [getHeadingLevelForChapter()](#getHeadingLevelForChapter) | Gibt den Überschriften‑Stil zurück, der auf die Kapiteltitel im Dokument angewendet wird. |
| [getLayoutMode()](#getLayoutMode) | Gibt den Layout‑Modus dieses Abschnitts zurück. |
| [getLeftMargin()](#getLeftMargin) | Ermittelt den Abstand (in Punkten) zwischen dem linken Rand der Seite und der linken Begrenzung des Fließtextes. |
| [getLineNumberCountBy()](#getLineNumberCountBy) | Ermittelt die numerische Erhöhung für Zeilennummern. |
| [getLineNumberDistanceFromText()](#getLineNumberDistanceFromText) | Ermittelt den Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments. |
| [getLineNumberRestartMode()](#getLineNumberRestartMode) | Ermittelt, wie die Zeilennummerierung verläuft, d. h. ob sie am Anfang einer neuen Seite oder Abschnitt neu beginnt oder kontinuierlich läuft. |
| [getLineStartingNumber()](#getLineStartingNumber) | Ermittelt die Startzeilennummer. |
| [getLinesPerPage()](#getLinesPerPage) | Ermittelt die Anzahl der Zeilen pro Seite im Dokumentgitter. |
| [getMargins()](#getMargins) | Ermittelt die voreingestellten [Margins](../../com.aspose.words/margins/) der Seite. |
| [getMultiplePages()](#getMultiplePages) | Für mehrseitige Dokumente ermittelt oder legt fest, wie ein Dokument gedruckt oder gerendert wird, damit es als Heft gebunden werden kann. |
| [getOddAndEvenPagesHeaderFooter()](#getOddAndEvenPagesHeaderFooter) | True, wenn das Dokument unterschiedliche Kopf‑ und Fußzeilen für ungerade und gerade Seiten hat. |
| [getOrientation()](#getOrientation) | Ermittelt die Ausrichtung der Seite. |
| [getOtherPagesTray()](#getOtherPagesTray) | Ermittelt das Papierfach (Behälter), das für alle Seiten außer der ersten Seite eines Abschnitts verwendet wird. |
| [getPageHeight()](#getPageHeight) | Ermittelt die Höhe der Seite in Punkten. |
| [getPageNumberStyle()](#getPageNumberStyle) | Ermittelt das Seitenzahlenformat. |
| [getPageStartingNumber()](#getPageStartingNumber) | Ermittelt die Startseitenzahl des Abschnitts. |
| [getPageWidth()](#getPageWidth) | Ermittelt die Breite der Seite in Punkten. |
| [getPaperSize()](#getPaperSize) | Ermittelt die Papiergröße. |
| [getRestartPageNumbering()](#getRestartPageNumbering) | True, wenn die Seitennummerierung am Anfang des Abschnitts neu beginnt. |
| [getRightMargin()](#getRightMargin) | Ermittelt den Abstand (in Punkten) zwischen dem rechten Rand der Seite und der rechten Begrenzung des Fließtextes. |
| [getRtlGutter()](#getRtlGutter) | Ermittelt, ob Microsoft Word für den Abschnitt Ränder (Gutters) basierend auf einer Rechts‑nach‑Links‑ oder Links‑nach‑Rechts‑Sprache verwendet. |
| [getSectionStart()](#getSectionStart) | Ermittelt den Typ des Abschnittsumbruchs für das angegebene Objekt. |
| [getSheetsPerBooklet()](#getSheetsPerBooklet) | Ermittelt die Anzahl der Seiten, die in jedes Heft aufgenommen werden. |
| [getSuppressEndnotes()](#getSuppressEndnotes) | True, wenn Endnoten am Ende des nächsten Abschnitts gedruckt werden, der Endnoten nicht unterdrückt. |
| [getTextColumns()](#getTextColumns) | Gibt eine Sammlung zurück, die die Menge der Textspalten darstellt. |
| [getTextOrientation()](#getTextOrientation) | Ermöglicht die Angabe von [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) für die gesamte Seite. |
| [getTopMargin()](#getTopMargin) | Ermittelt den Abstand (in Punkten) zwischen dem oberen Rand der Seite und der oberen Begrenzung des Fließtextes. |
| [getVerticalAlignment()](#getVerticalAlignment) | Ermittelt die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder Abschnitt. |
| [setBidi(boolean value)](#setBidi-boolean) | Gibt an, dass dieser Abschnitt bidirektionalen (komplexen Skript‑) Text enthält. |
| [setBorderAlwaysInFront(boolean value)](#setBorderAlwaysInFront-boolean) | Gibt an, wo der Seitenrand relativ zu sich kreuzenden Texten und Objekten positioniert ist. |
| [setBorderAppliesTo(int value)](#setBorderAppliesTo-int) | Gibt an, auf welchen Seiten der Seitenrand gedruckt wird. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBorderDistanceFrom(int value)](#setBorderDistanceFrom-int) | Legt einen Wert fest, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umgebenden Text gemessen wird. |
| [setBorderSurroundsFooter(boolean value)](#setBorderSurroundsFooter-boolean) | Gibt an, ob der Seitenrand die Fußzeile ein- oder ausschließt. |
| [setBorderSurroundsHeader(boolean value)](#setBorderSurroundsHeader-boolean) | Gibt an, ob der Seitenrand die Kopfzeile ein- oder ausschließt. |
| [setBottomMargin(double value)](#setBottomMargin-double) | Legt den Abstand (in Punkten) zwischen dem unteren Rand der Seite und der unteren Begrenzung des Fließtextes fest. |
| [setChapterPageSeparator(int value)](#setChapterPageSeparator-int) | Legt das Trennzeichen fest, das zwischen der Kapitelnummer und der Seitenzahl erscheint. |
| [setCharactersPerLine(int value)](#setCharactersPerLine-int) | Legt die Anzahl der Zeichen pro Zeile im Dokumentgitter fest. |
| [setDifferentFirstPageHeaderFooter(boolean value)](#setDifferentFirstPageHeaderFooter-boolean) | Wahr, wenn auf der ersten Seite eine andere Kopf‑ oder Fußzeile verwendet wird. |
| [setFirstPageTray(int value)](#setFirstPageTray-int) | Legt das Papierfach (Bin) fest, das für die erste Seite eines Abschnitts verwendet wird. |
| [setFooterDistance(double value)](#setFooterDistance-double) | Legt den Abstand (in Punkten) zwischen der Fußzeile und dem unteren Rand der Seite fest. |
| [setGutter(double value)](#setGutter-double) | Legt die Menge des zusätzlichen Raums fest, der dem Rand für die Dokumentbindung hinzugefügt wird. |
| [setHeaderDistance(double value)](#setHeaderDistance-double) | Legt den Abstand (in Punkten) zwischen der Kopfzeile und dem oberen Rand der Seite fest. |
| [setHeadingLevelForChapter(int value)](#setHeadingLevelForChapter-int) | Legt den Überschriftsstil fest, der auf die Kapiteltitel im Dokument angewendet wird. |
| [setLayoutMode(int value)](#setLayoutMode-int) | Legt den Layoutmodus dieses Abschnitts fest. |
| [setLeftMargin(double value)](#setLeftMargin-double) | Legt den Abstand (in Punkten) zwischen dem linken Rand der Seite und der linken Begrenzung des Fließtextes fest. |
| [setLineNumberCountBy(int value)](#setLineNumberCountBy-int) | Legt die numerische Erhöhung für Zeilennummern fest. |
| [setLineNumberDistanceFromText(double value)](#setLineNumberDistanceFromText-double) | Legt den Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments fest. |
| [setLineNumberRestartMode(int value)](#setLineNumberRestartMode-int) | Legt fest, wie die Zeilennummerierung verläuft, also ob sie am Anfang einer neuen Seite oder eines neuen Abschnitts neu beginnt oder kontinuierlich weiterläuft. |
| [setLineStartingNumber(int value)](#setLineStartingNumber-int) | Legt die Startzeilennummer fest. |
| [setLinesPerPage(int value)](#setLinesPerPage-int) | Legt die Anzahl der Zeilen pro Seite im Dokumentgitter fest. |
| [setMargins(int value)](#setMargins-int) | Legt voreingestellte [Margins](../../com.aspose.words/margins/) der Seite fest. |
| [setMultiplePages(int value)](#setMultiplePages-int) | Für mehrseitige Dokumente ermittelt oder legt fest, wie ein Dokument gedruckt oder gerendert wird, damit es als Heft gebunden werden kann. |
| [setOddAndEvenPagesHeaderFooter(boolean value)](#setOddAndEvenPagesHeaderFooter-boolean) | True, wenn das Dokument unterschiedliche Kopf‑ und Fußzeilen für ungerade und gerade Seiten hat. |
| [setOrientation(int value)](#setOrientation-int) | Legt die Ausrichtung der Seite fest. |
| [setOtherPagesTray(int value)](#setOtherPagesTray-int) | Legt das Papierfach (Bin) fest, das für alle Seiten außer der ersten Seite eines Abschnitts verwendet wird. |
| [setPageHeight(double value)](#setPageHeight-double) | Legt die Höhe der Seite in Punkten fest. |
| [setPageNumberStyle(int value)](#setPageNumberStyle-int) | Legt das Seitenzahlenformat fest. |
| [setPageStartingNumber(int value)](#setPageStartingNumber-int) | Legt die Startseitenzahl des Abschnitts fest. |
| [setPageWidth(double value)](#setPageWidth-double) | Legt die Breite der Seite in Punkten fest. |
| [setPaperSize(int value)](#setPaperSize-int) | Legt die Papiergröße fest. |
| [setRestartPageNumbering(boolean value)](#setRestartPageNumbering-boolean) | True, wenn die Seitennummerierung am Anfang des Abschnitts neu beginnt. |
| [setRightMargin(double value)](#setRightMargin-double) | Legt den Abstand (in Punkten) zwischen dem rechten Rand der Seite und der rechten Begrenzung des Fließtextes fest. |
| [setRtlGutter(boolean value)](#setRtlGutter-boolean) | Legt fest, ob Microsoft Word für den Abschnitt Ränder verwendet, basierend auf einer Rechts-nach-Links- oder Links-nach-Rechts-Sprache. |
| [setSectionStart(int value)](#setSectionStart-int) | Legt den Typ des Abschnittsumbruchs für das angegebene Objekt fest. |
| [setSheetsPerBooklet(int value)](#setSheetsPerBooklet-int) | Legt die Anzahl der Seiten fest, die in jedes Heft aufgenommen werden. |
| [setSuppressEndnotes(boolean value)](#setSuppressEndnotes-boolean) | True, wenn Endnoten am Ende des nächsten Abschnitts gedruckt werden, der Endnoten nicht unterdrückt. |
| [setTextOrientation(int value)](#setTextOrientation-int) | Ermöglicht die Angabe von [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) für die gesamte Seite. |
| [setTopMargin(double value)](#setTopMargin-double) | Legt den Abstand (in Punkten) zwischen dem oberen Rand der Seite und der oberen Begrenzung des Fließtextes fest. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Legt die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder Abschnitt fest. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Setzt die Seiteneinrichtung auf die Standard‑Papiergröße, Ränder und Ausrichtung zurück.

 **Examples:** 

Zeigt, wie man Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument anwendet und zurücksetzt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Gibt an, dass dieser Abschnitt bidirektionalen (komplexen Skript‑) Text enthält.

 **Remarks:** 

Wenn true, werden die Spalten in diesem Abschnitt von rechts nach links angeordnet.

 **Examples:** 

Zeigt, wie die Reihenfolge der Textspalten in einem Abschnitt festgelegt wird.

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
boolean - Der entsprechende  boolean  Wert.
### getBorderAlwaysInFront() {#getBorderAlwaysInFront}
```
public boolean getBorderAlwaysInFront()
```


Gibt an, wo der Seitenrand relativ zu sich kreuzenden Texten und Objekten positioniert ist.

 **Examples:** 

Zeigt, wie man einen breiten blauen Bandrahmen oben auf der ersten Seite erstellt.

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
boolean - Der entsprechende  boolean  Wert.
### getBorderAppliesTo() {#getBorderAppliesTo}
```
public int getBorderAppliesTo()
```


Gibt an, auf welchen Seiten der Seitenrand gedruckt wird.

 **Examples:** 

Zeigt, wie man einen breiten blauen Bandrahmen oben auf der ersten Seite erstellt.

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
int - Der entsprechende int-Wert. Der zurückgegebene Wert ist einer der [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/) Konstanten.
### getBorderDistanceFrom() {#getBorderDistanceFrom}
```
public int getBorderDistanceFrom()
```


Gibt einen Wert zurück, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umschlossenen Text gemessen wird.

 **Examples:** 

Zeigt, wie man einen breiten blauen Bandrahmen oben auf der ersten Seite erstellt.

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
int - Ein Wert, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umgebenden Text gemessen wird. Der zurückgegebene Wert ist einer der [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/) Konstanten.
### getBorderSurroundsFooter() {#getBorderSurroundsFooter}
```
public boolean getBorderSurroundsFooter()
```


Gibt an, ob der Seitenrand die Fußzeile ein- oder ausschließt.

 **Remarks:** 

Hinweis: Das Ändern dieser Eigenschaft wirkt sich auf alle Abschnitte im Dokument aus.

 **Examples:** 

Zeigt, wie ein Rand auf die Seite sowie Kopf- und Fußzeile angewendet wird.

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
boolean - Der entsprechende  boolean  Wert.
### getBorderSurroundsHeader() {#getBorderSurroundsHeader}
```
public boolean getBorderSurroundsHeader()
```


Gibt an, ob der Seitenrand die Kopfzeile ein- oder ausschließt.

 **Remarks:** 

Hinweis: Das Ändern dieser Eigenschaft wirkt sich auf alle Abschnitte im Dokument aus.

 **Examples:** 

Zeigt, wie ein Rand auf die Seite sowie Kopf- und Fußzeile angewendet wird.

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
boolean - Der entsprechende  boolean  Wert.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Gibt eine Sammlung der Seitenränder zurück.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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


Gibt den Abstand (in Punkten) zwischen dem unteren Rand der Seite und der unteren Begrenzung des Fließtextes zurück.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
double - Der Abstand (in Punkten) zwischen dem unteren Rand der Seite und der unteren Begrenzung des Fließtextes.
### getChapterPageSeparator() {#getChapterPageSeparator}
```
public int getChapterPageSeparator()
```


Gibt das Trennzeichen zurück, das zwischen Kapitelnummer und Seitenzahl erscheint.

 **Remarks:** 

Bevor Sie Seitenzahlen erstellen können, die Kapitelnummern enthalten, müssen die Dokumentüberschriften ein nummeriertes Gliederungsformat besitzen.

 **Examples:** 

Zeigt, wie man mit Seitenkapiteln arbeitet.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - Das Trennzeichen, das zwischen der Kapitelnummer und der Seitenzahl erscheint. Der zurückgegebene Wert ist einer der [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/) Konstanten.
### getCharactersPerLine() {#getCharactersPerLine}
```
public int getCharactersPerLine()
```


Gibt die Anzahl der Zeichen pro Zeile im Dokumentgitter zurück.

 **Remarks:** 

Der Mindestwert der Eigenschaft ist 1. Der Höchstwert hängt von der Seitenbreite und der Schriftgröße des Normal-Stils ab. Der minimale Zeichenabstand beträgt 90 Prozent der Schriftgröße. Zum Beispiel beträgt die maximale Zeichenanzahl pro Zeile einer Letter-Seite mit ein‑Zoll‑Rändern 43.

Standardmäßig hat die Eigenschaft einen Wert, bei dem der Zeichenabstand der Schriftgröße des Normal-Stils entspricht.

 **Examples:** 

Zeigt, wie man eine Begrenzung für die Anzahl der Zeichen festlegt, die jede Zeile haben darf.

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
int - Die Anzahl der Zeichen pro Zeile im Dokumentgitter.
### getDifferentFirstPageHeaderFooter() {#getDifferentFirstPageHeaderFooter}
```
public boolean getDifferentFirstPageHeaderFooter()
```


Wahr, wenn auf der ersten Seite eine andere Kopf‑ oder Fußzeile verwendet wird.

 **Examples:** 

Zeigt, wie man Kopf- und Fußzeilen in einem Dokument mit DocumentBuilder erstellt.

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

Zeigt, wie die Reihenfolge verfolgt wird, in der ein Textaustauschvorgang Knoten durchläuft.

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

Zeigt, wie primäre Kopf‑ und Fußzeilen aktiviert oder deaktiviert werden.

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
boolean - Der entsprechende  boolean  Wert.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getEndnoteOptions() {#getEndnoteOptions}
```
public EndnoteOptions getEndnoteOptions()
```


Bietet Optionen, die die Nummerierung und Positionierung von Endnoten in diesem Abschnitt steuern.

 **Examples:** 

Zeigt, wie Optionen konfiguriert werden, die Fuß‑ und Endnoten in einem Abschnitt beeinflussen.

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


Ermittelt das Papierfach (Bin), das für die erste Seite eines Abschnitts verwendet wird. Der Wert ist implementierungs‑ (Drucker‑) spezifisch.

 **Examples:** 

Zeigt, wie das Drucken mit verschiedenen Druckerfächern für unterschiedliche Papierformate eingerichtet wird.

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
int - Das Papierfach (Bin), das für die erste Seite eines Abschnitts verwendet wird.
### getFooterDistance() {#getFooterDistance}
```
public double getFooterDistance()
```


Gibt den Abstand (in Punkten) zwischen der Fußzeile und dem unteren Rand der Seite zurück.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
double - Der Abstand (in Punkten) zwischen der Fußzeile und dem unteren Rand der Seite.
### getFootnoteOptions() {#getFootnoteOptions}
```
public FootnoteOptions getFootnoteOptions()
```


Bietet Optionen, die die Nummerierung und Positionierung von Fußnoten in diesem Abschnitt steuern.

 **Examples:** 

Zeigt, wie Optionen konfiguriert werden, die Fuß‑ und Endnoten in einem Abschnitt beeinflussen.

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


Gibt die Menge des zusätzlichen Raums zurück, der dem Rand für die Dokumentbindung hinzugefügt wird.

 **Examples:** 

Zeigt, wie man Bundsteg‑Ränder festlegt.

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

Zeigt, wie man ein Dokument konfiguriert, das als Buchfalz gedruckt werden kann.

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
double - Die Menge an zusätzlichem Raum, die dem Rand für die Dokumentbindung hinzugefügt wird.
### getHeaderDistance() {#getHeaderDistance}
```
public double getHeaderDistance()
```


Gibt den Abstand (in Punkten) zwischen der Kopfzeile und dem oberen Rand der Seite zurück.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
double - Der Abstand (in Punkten) zwischen der Kopfzeile und dem oberen Rand der Seite.
### getHeadingLevelForChapter() {#getHeadingLevelForChapter}
```
public int getHeadingLevelForChapter()
```


Gibt den Überschriften‑Stil zurück, der auf die Kapiteltitel im Dokument angewendet wird.

 **Remarks:** 

Kann eine Zahl von 0 bis 9 sein. 0 bedeutet keine Kapitelnummer, wenn sie auf die Seitenzahl angewendet wird.

Bevor Sie Seitenzahlen erstellen können, die Kapitelnummern enthalten, müssen die Dokumentüberschriften ein nummeriertes Gliederungsformat besitzen.

 **Examples:** 

Zeigt, wie man mit Seitenkapiteln arbeitet.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - Der Überschriften‑Ebenen‑Stil, der auf die Kapiteltitel im Dokument angewendet wird.
### getLayoutMode() {#getLayoutMode}
```
public int getLayoutMode()
```


Gibt den Layout‑Modus dieses Abschnitts zurück.

 **Examples:** 

Zeigt, wie man eine Begrenzung für die Anzahl der Zeichen festlegt, die jede Zeile haben darf.

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

Zeigt, wie man ein Limit für die Zeilenanzahl festlegt, die jede Seite haben darf.

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
int - Der Layout‑Modus dieses Abschnitts. Der zurückgegebene Wert ist einer der Konstanten von [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/).
### getLeftMargin() {#getLeftMargin}
```
public double getLeftMargin()
```


Ermittelt den Abstand (in Punkten) zwischen dem linken Rand der Seite und der linken Begrenzung des Fließtextes.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
double - Der Abstand (in Punkten) zwischen dem linken Rand der Seite und der linken Begrenzung des Fließtextes.
### getLineNumberCountBy() {#getLineNumberCountBy}
```
public int getLineNumberCountBy()
```


Ermittelt die numerische Erhöhung für Zeilennummern.

 **Examples:** 

Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.

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
int - Der numerische Inkrement für Zeilennummern.
### getLineNumberDistanceFromText() {#getLineNumberDistanceFromText}
```
public double getLineNumberDistanceFromText()
```


Ermittelt den Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments.

 **Remarks:** 

Setzen Sie diese Eigenschaft auf Null, um einen automatischen Abstand zwischen den Zeilennummern und dem Text des Dokuments zu erhalten.

 **Examples:** 

Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.

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
double - Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments.
### getLineNumberRestartMode() {#getLineNumberRestartMode}
```
public int getLineNumberRestartMode()
```


Ermittelt, wie die Zeilennummerierung verläuft, d. h. ob sie am Anfang einer neuen Seite oder Abschnitt neu beginnt oder kontinuierlich läuft.

 **Examples:** 

Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.

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
int - Die Art, wie die Zeilennummerierung verläuft, d. h. ob sie am Anfang einer neuen Seite oder eines neuen Abschnitts neu beginnt oder kontinuierlich weiterläuft. Der zurückgegebene Wert ist einer der Konstanten von [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/).
### getLineStartingNumber() {#getLineStartingNumber}
```
public int getLineStartingNumber()
```


Ermittelt die Startzeilennummer.

 **Examples:** 

Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.

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
int - Die startende Zeilennummer.
### getLinesPerPage() {#getLinesPerPage}
```
public int getLinesPerPage()
```


Ermittelt die Anzahl der Zeilen pro Seite im Dokumentgitter.

 **Remarks:** 

Der Minimalwert dieser Eigenschaft ist 1. Der Maximalwert hängt von der Seitenhöhe und der Schriftgröße des Normal‑Stils ab. Der minimale Zeilenabstand beträgt 136 % der Schriftgröße. Zum Beispiel beträgt die maximale Zeilenanzahl pro Seite eines Letter‑Formats mit ein‑Zoll‑Rändern 39.

Standardmäßig hat die Eigenschaft einen Wert, bei dem der Zeilenabstand das 1,5‑fache der Schriftgröße des Normal‑Stils beträgt.

 **Examples:** 

Zeigt, wie man ein Limit für die Zeilenanzahl festlegt, die jede Seite haben darf.

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
int - Die Anzahl der Zeilen pro Seite im Dokumentgitter.
### getMargins() {#getMargins}
```
public int getMargins()
```


Ermittelt die voreingestellten [Margins](../../com.aspose.words/margins/) der Seite.

 **Examples:** 

Zeigt, wann das Seitenlayout des Dokuments neu berechnet werden soll.

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
int - Vorgabewert für die [Margins](../../com.aspose.words/margins/) der Seite. Der zurückgegebene Wert ist einer der Konstanten von [Margins](../../com.aspose.words/margins/).
### getMultiplePages() {#getMultiplePages}
```
public int getMultiplePages()
```


Für mehrseitige Dokumente ermittelt oder legt fest, wie ein Dokument gedruckt oder gerendert wird, damit es als Heft gebunden werden kann.

 **Examples:** 

Zeigt, wie man Bundsteg‑Ränder festlegt.

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

Zeigt, wie man ein Dokument konfiguriert, das als Buchfalz gedruckt werden kann.

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
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [MultiplePagesType](../../com.aspose.words/multiplepagestype/).
### getOddAndEvenPagesHeaderFooter() {#getOddAndEvenPagesHeaderFooter}
```
public boolean getOddAndEvenPagesHeaderFooter()
```


True, wenn das Dokument unterschiedliche Kopf‑ und Fußzeilen für ungerade und gerade Seiten hat.

 **Remarks:** 

Hinweis: Das Ändern dieser Eigenschaft wirkt sich auf alle Abschnitte im Dokument aus.

 **Examples:** 

Zeigt, wie man Kopf- und Fußzeilen in einem Dokument mit DocumentBuilder erstellt.

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

Zeigt, wie man gerade Seiten‑Kopf‑/Fußzeilen aktiviert oder deaktiviert.

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
boolean - Der entsprechende  boolean  Wert.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Ermittelt die Ausrichtung der Seite.

 **Remarks:** 

Das Ändern von [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int) vertauscht [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) und [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double).

 **Examples:** 

Zeigt, wie man Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument anwendet und zurücksetzt.

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

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
int - Die Orientierung der Seite. Der zurückgegebene Wert ist einer der Konstanten von [Orientation](../../com.aspose.words/orientation/).
### getOtherPagesTray() {#getOtherPagesTray}
```
public int getOtherPagesTray()
```


Ermittelt das Papierfach (Behälter), das für alle Seiten außer der ersten Seite eines Abschnitts verwendet wird. Der Wert ist implementationsspezifisch (Drucker).

 **Examples:** 

Zeigt, wie das Drucken mit verschiedenen Druckerfächern für unterschiedliche Papierformate eingerichtet wird.

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
int – Das Papierfach (Behälter), das für alle Seiten außer der ersten Seite eines Abschnitts verwendet wird.
### getPageHeight() {#getPageHeight}
```
public double getPageHeight()
```


Ermittelt die Höhe der Seite in Punkten.

 **Examples:** 

Zeigt, wie man ein Bild einfügt und es als Wasserzeichen verwendet.

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
double – Die Höhe der Seite in Punkten.
### getPageNumberStyle() {#getPageNumberStyle}
```
public int getPageNumberStyle()
```


Ermittelt das Seitenzahlenformat.

 **Examples:** 

Zeigt, wie man die Seitennummerierung in einem Abschnitt einrichtet.

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
int – Das Format der Seitennummer. Der zurückgegebene Wert ist einer der [NumberStyle](../../com.aspose.words/numberstyle/) Konstanten.
### getPageStartingNumber() {#getPageStartingNumber}
```
public int getPageStartingNumber()
```


Ermittelt die Startseitenzahl des Abschnitts.

 **Remarks:** 

Die [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) Eigenschaft, wenn sie auf false gesetzt ist, überschreibt die [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) Eigenschaft, sodass die Seitennummerierung vom vorherigen Abschnitt fortgesetzt werden kann.

 **Examples:** 

Zeigt, wie man die Seitennummerierung in einem Abschnitt einrichtet.

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
int – Die Startseitennummer des Abschnitts.
### getPageWidth() {#getPageWidth}
```
public double getPageWidth()
```


Ermittelt die Breite der Seite in Punkten.

 **Examples:** 

Zeigt, wie man ein Bild einfügt und es als Wasserzeichen verwendet.

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

Zeigt, wie man ein schwebendes Bild einfügt und dessen Position und Größe festlegt.

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
double – Die Breite der Seite in Punkten.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Ermittelt die Papiergröße.

 **Remarks:** 

Das Setzen dieser Eigenschaft aktualisiert die Werte von [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) und [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double). Das Setzen dieses Werts auf [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) ändert die bestehenden Werte nicht.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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

Zeigt, wie man Seitengrößen festlegt.

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

Zeigt, wie man die Papiergröße von JisB4 oder JisB5 festlegt.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

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
int – Die Papiergröße. Der zurückgegebene Wert ist einer der [PaperSize](../../com.aspose.words/papersize/) Konstanten.
### getRestartPageNumbering() {#getRestartPageNumbering}
```
public boolean getRestartPageNumbering()
```


True, wenn die Seitennummerierung am Anfang des Abschnitts neu beginnt.

 **Remarks:** 

Wenn sie auf false gesetzt ist, überschreibt die [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) Eigenschaft die [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) Eigenschaft, sodass die Seitennummerierung vom vorherigen Abschnitt fortgesetzt werden kann.

 **Examples:** 

Zeigt, wie man die Seitennummerierung in einem Abschnitt einrichtet.

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
boolean - Der entsprechende  boolean  Wert.
### getRightMargin() {#getRightMargin}
```
public double getRightMargin()
```


Ermittelt den Abstand (in Punkten) zwischen dem rechten Rand der Seite und der rechten Begrenzung des Fließtextes.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
double – Der Abstand (in Punkten) zwischen dem rechten Rand der Seite und der rechten Begrenzung des Fließtextes.
### getRtlGutter() {#getRtlGutter}
```
public boolean getRtlGutter()
```


Ermittelt, ob Microsoft Word für den Abschnitt Ränder (Gutters) basierend auf einer Rechts‑nach‑Links‑ oder Links‑nach‑Rechts‑Sprache verwendet.

 **Examples:** 

Zeigt, wie man Bundsteg‑Ränder festlegt.

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
boolean – Ob Microsoft Word für den Abschnitt Gutter verwendet, abhängig von einer Rechts-nach-Links- oder Links-nach-Rechts-Sprache.
### getSectionStart() {#getSectionStart}
```
public int getSectionStart()
```


Ermittelt den Typ des Abschnittsumbruchs für das angegebene Objekt.

 **Examples:** 

Zeigt, wie man festlegt, wie ein neuer Abschnitt sich vom vorherigen trennt.

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

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

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
int – Der Typ des Abschnittsumbruchs für das angegebene Objekt. Der zurückgegebene Wert ist einer der [SectionStart](../../com.aspose.words/sectionstart/) Konstanten.
### getSheetsPerBooklet() {#getSheetsPerBooklet}
```
public int getSheetsPerBooklet()
```


Ermittelt die Anzahl der Seiten, die in jedes Heft aufgenommen werden.

 **Examples:** 

Zeigt, wie man ein Dokument konfiguriert, das als Buchfalz gedruckt werden kann.

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
int – Die Anzahl der Seiten, die in jedem Heft enthalten sein sollen.
### getSuppressEndnotes() {#getSuppressEndnotes}
```
public boolean getSuppressEndnotes()
```


True, wenn Endnoten am Ende des nächsten Abschnitts gedruckt werden, der Endnoten nicht unterdrückt. Unterdrückte Endnoten werden vor den Endnoten in diesem Abschnitt gedruckt.

 **Examples:** 

Zeigt, wie man Endnoten am Ende jedes Abschnitts speichert und deren Positionen ändert.

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
boolean - Der entsprechende  boolean  Wert.
### getTextColumns() {#getTextColumns}
```
public TextColumnCollection getTextColumns()
```


Gibt eine Sammlung zurück, die die Menge der Textspalten darstellt.

 **Examples:** 

Zeigt, wie man in einem Abschnitt mehrere gleichmäßig verteilte Spalten erstellt.

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


Ermöglicht das Festlegen von [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) für die gesamte Seite. Der Standardwert ist [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL)

 **Remarks:** 

Diese Eigenschaft wird nur für die nativen MS‑Word‑Formate DOCX, WML, RTF und DOC unterstützt.

 **Examples:** 

Zeigt, wie die Textausrichtung festgelegt wird.

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
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [TextOrientation](../../com.aspose.words/textorientation/).
### getTopMargin() {#getTopMargin}
```
public double getTopMargin()
```


Ermittelt den Abstand (in Punkten) zwischen dem oberen Rand der Seite und der oberen Begrenzung des Fließtextes.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
double – Der Abstand (in Punkten) zwischen der oberen Kante der Seite und der oberen Begrenzung des Fließtextes.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Ermittelt die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder Abschnitt.

 **Examples:** 

Zeigt, wie man Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument anwendet und zurücksetzt.

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
int – Die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder Abschnitt. Der zurückgegebene Wert ist einer der Konstanten von [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/).
### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Gibt an, dass dieser Abschnitt bidirektionalen (komplexen Skript‑) Text enthält.

 **Remarks:** 

Wenn true, werden die Spalten in diesem Abschnitt von rechts nach links angeordnet.

 **Examples:** 

Zeigt, wie die Reihenfolge der Textspalten in einem Abschnitt festgelegt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBorderAlwaysInFront(boolean value) {#setBorderAlwaysInFront-boolean}
```
public void setBorderAlwaysInFront(boolean value)
```


Gibt an, wo der Seitenrand relativ zu sich kreuzenden Texten und Objekten positioniert ist.

 **Examples:** 

Zeigt, wie man einen breiten blauen Bandrahmen oben auf der ersten Seite erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBorderAppliesTo(int value) {#setBorderAppliesTo-int}
```
public void setBorderAppliesTo(int value)
```


Gibt an, auf welchen Seiten der Seitenrand gedruckt wird.

 **Examples:** 

Zeigt, wie man einen breiten blauen Bandrahmen oben auf der ersten Seite erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/) sein. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

### setBorderDistanceFrom(int value) {#setBorderDistanceFrom-int}
```
public void setBorderDistanceFrom(int value)
```


Legt einen Wert fest, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umgebenden Text gemessen wird.

 **Examples:** 

Zeigt, wie man einen breiten blauen Bandrahmen oben auf der ersten Seite erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Ein Wert, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umgebenden Text gemessen wird. Der Wert muss einer der Konstanten von [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/) sein. |

### setBorderSurroundsFooter(boolean value) {#setBorderSurroundsFooter-boolean}
```
public void setBorderSurroundsFooter(boolean value)
```


Gibt an, ob der Seitenrand die Fußzeile ein- oder ausschließt.

 **Remarks:** 

Hinweis: Das Ändern dieser Eigenschaft wirkt sich auf alle Abschnitte im Dokument aus.

 **Examples:** 

Zeigt, wie ein Rand auf die Seite sowie Kopf- und Fußzeile angewendet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBorderSurroundsHeader(boolean value) {#setBorderSurroundsHeader-boolean}
```
public void setBorderSurroundsHeader(boolean value)
```


Gibt an, ob der Seitenrand die Kopfzeile ein- oder ausschließt.

 **Remarks:** 

Hinweis: Das Ändern dieser Eigenschaft wirkt sich auf alle Abschnitte im Dokument aus.

 **Examples:** 

Zeigt, wie ein Rand auf die Seite sowie Kopf- und Fußzeile angewendet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBottomMargin(double value) {#setBottomMargin-double}
```
public void setBottomMargin(double value)
```


Legt den Abstand (in Punkten) zwischen dem unteren Rand der Seite und der unteren Begrenzung des Fließtextes fest.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Abstand (in Punkten) zwischen der unteren Kante der Seite und der unteren Begrenzung des Fließtextes. |

### setChapterPageSeparator(int value) {#setChapterPageSeparator-int}
```
public void setChapterPageSeparator(int value)
```


Legt das Trennzeichen fest, das zwischen der Kapitelnummer und der Seitenzahl erscheint.

 **Remarks:** 

Bevor Sie Seitenzahlen erstellen können, die Kapitelnummern enthalten, müssen die Dokumentüberschriften ein nummeriertes Gliederungsformat besitzen.

 **Examples:** 

Zeigt, wie man mit Seitenkapiteln arbeitet.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Das Trennzeichen, das zwischen Kapitelnummer und Seitenzahl erscheint. Der Wert muss einer der Konstanten von [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/) sein. |

### setCharactersPerLine(int value) {#setCharactersPerLine-int}
```
public void setCharactersPerLine(int value)
```


Legt die Anzahl der Zeichen pro Zeile im Dokumentgitter fest.

 **Remarks:** 

Der Mindestwert der Eigenschaft ist 1. Der Höchstwert hängt von der Seitenbreite und der Schriftgröße des Normal-Stils ab. Der minimale Zeichenabstand beträgt 90 Prozent der Schriftgröße. Zum Beispiel beträgt die maximale Zeichenanzahl pro Zeile einer Letter-Seite mit ein‑Zoll‑Rändern 43.

Standardmäßig hat die Eigenschaft einen Wert, bei dem der Zeichenabstand der Schriftgröße des Normal-Stils entspricht.

 **Examples:** 

Zeigt, wie man eine Begrenzung für die Anzahl der Zeichen festlegt, die jede Zeile haben darf.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Anzahl der Zeichen pro Zeile im Dokumentengitter. |

### setDifferentFirstPageHeaderFooter(boolean value) {#setDifferentFirstPageHeaderFooter-boolean}
```
public void setDifferentFirstPageHeaderFooter(boolean value)
```


Wahr, wenn auf der ersten Seite eine andere Kopf‑ oder Fußzeile verwendet wird.

 **Examples:** 

Zeigt, wie man Kopf- und Fußzeilen in einem Dokument mit DocumentBuilder erstellt.

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

Zeigt, wie die Reihenfolge verfolgt wird, in der ein Textaustauschvorgang Knoten durchläuft.

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

Zeigt, wie primäre Kopf‑ und Fußzeilen aktiviert oder deaktiviert werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setFirstPageTray(int value) {#setFirstPageTray-int}
```
public void setFirstPageTray(int value)
```


Legt das Papierfach (Bin) fest, das für die erste Seite eines Abschnitts verwendet wird. Der Wert ist implementierungs‑ (Drucker‑) spezifisch.

 **Examples:** 

Zeigt, wie das Drucken mit verschiedenen Druckerfächern für unterschiedliche Papierformate eingerichtet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Das Papierfach (Bin), das für die erste Seite eines Abschnitts verwendet wird. |

### setFooterDistance(double value) {#setFooterDistance-double}
```
public void setFooterDistance(double value)
```


Legt den Abstand (in Punkten) zwischen der Fußzeile und dem unteren Rand der Seite fest.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Abstand (in Punkten) zwischen der Fußzeile und dem unteren Rand der Seite. |

### setGutter(double value) {#setGutter-double}
```
public void setGutter(double value)
```


Legt die Menge des zusätzlichen Raums fest, der dem Rand für die Dokumentbindung hinzugefügt wird.

 **Examples:** 

Zeigt, wie man Bundsteg‑Ränder festlegt.

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

Zeigt, wie man ein Dokument konfiguriert, das als Buchfalz gedruckt werden kann.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der zusätzliche Abstand, der dem Rand für die Dokumentbindung hinzugefügt wird. |

### setHeaderDistance(double value) {#setHeaderDistance-double}
```
public void setHeaderDistance(double value)
```


Legt den Abstand (in Punkten) zwischen der Kopfzeile und dem oberen Rand der Seite fest.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Abstand (in Punkten) zwischen der Kopfzeile und dem oberen Rand der Seite. |

### setHeadingLevelForChapter(int value) {#setHeadingLevelForChapter-int}
```
public void setHeadingLevelForChapter(int value)
```


Legt den Überschriftsstil fest, der auf die Kapiteltitel im Dokument angewendet wird.

 **Remarks:** 

Kann eine Zahl von 0 bis 9 sein. 0 bedeutet keine Kapitelnummer, wenn sie auf die Seitenzahl angewendet wird.

Bevor Sie Seitenzahlen erstellen können, die Kapitelnummern enthalten, müssen die Dokumentüberschriften ein nummeriertes Gliederungsformat besitzen.

 **Examples:** 

Zeigt, wie man mit Seitenkapiteln arbeitet.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Überschrifts‑Stil, der auf die Kapiteltitel im Dokument angewendet wird. |

### setLayoutMode(int value) {#setLayoutMode-int}
```
public void setLayoutMode(int value)
```


Legt den Layoutmodus dieses Abschnitts fest.

 **Examples:** 

Zeigt, wie man eine Begrenzung für die Anzahl der Zeichen festlegt, die jede Zeile haben darf.

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

Zeigt, wie man ein Limit für die Zeilenanzahl festlegt, die jede Seite haben darf.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Layout‑Modus dieses Abschnitts. Der Wert muss einer der Konstanten von [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/) sein. |

### setLeftMargin(double value) {#setLeftMargin-double}
```
public void setLeftMargin(double value)
```


Legt den Abstand (in Punkten) zwischen dem linken Rand der Seite und der linken Begrenzung des Fließtextes fest.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Abstand (in Punkten) zwischen der linken Kante der Seite und der linken Begrenzung des Fließtextes. |

### setLineNumberCountBy(int value) {#setLineNumberCountBy-int}
```
public void setLineNumberCountBy(int value)
```


Legt die numerische Erhöhung für Zeilennummern fest.

 **Examples:** 

Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der numerische Inkrementwert für Zeilennummern. |

### setLineNumberDistanceFromText(double value) {#setLineNumberDistanceFromText-double}
```
public void setLineNumberDistanceFromText(double value)
```


Legt den Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments fest.

 **Remarks:** 

Setzen Sie diese Eigenschaft auf Null, um einen automatischen Abstand zwischen den Zeilennummern und dem Text des Dokuments zu erhalten.

 **Examples:** 

Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Abstand zwischen der rechten Kante der Zeilennummern und der linken Kante des Dokuments. |

### setLineNumberRestartMode(int value) {#setLineNumberRestartMode-int}
```
public void setLineNumberRestartMode(int value)
```


Legt fest, wie die Zeilennummerierung verläuft, also ob sie am Anfang einer neuen Seite oder eines neuen Abschnitts neu beginnt oder kontinuierlich weiterläuft.

 **Examples:** 

Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Art, wie die Zeilennummerierung verläuft, also ob sie am Anfang einer neuen Seite oder eines neuen Abschnitts neu beginnt oder kontinuierlich weiterläuft. Der Wert muss einer der Konstanten von [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/) sein. |

### setLineStartingNumber(int value) {#setLineStartingNumber-int}
```
public void setLineStartingNumber(int value)
```


Legt die Startzeilennummer fest.

 **Examples:** 

Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die startende Zeilennummer. |

### setLinesPerPage(int value) {#setLinesPerPage-int}
```
public void setLinesPerPage(int value)
```


Legt die Anzahl der Zeilen pro Seite im Dokumentgitter fest.

 **Remarks:** 

Der Minimalwert dieser Eigenschaft ist 1. Der Maximalwert hängt von der Seitenhöhe und der Schriftgröße des Normal‑Stils ab. Der minimale Zeilenabstand beträgt 136 % der Schriftgröße. Zum Beispiel beträgt die maximale Zeilenanzahl pro Seite eines Letter‑Formats mit ein‑Zoll‑Rändern 39.

Standardmäßig hat die Eigenschaft einen Wert, bei dem der Zeilenabstand das 1,5‑fache der Schriftgröße des Normal‑Stils beträgt.

 **Examples:** 

Zeigt, wie man ein Limit für die Zeilenanzahl festlegt, die jede Seite haben darf.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Anzahl der Zeilen pro Seite im Dokumentengitter. |

### setMargins(int value) {#setMargins-int}
```
public void setMargins(int value)
```


Legt voreingestellte [Margins](../../com.aspose.words/margins/) der Seite fest.

 **Examples:** 

Zeigt, wann das Seitenlayout des Dokuments neu berechnet werden soll.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Voreingestellte [Margins](../../com.aspose.words/margins/) der Seite. Der Wert muss einer der Konstanten von [Margins](../../com.aspose.words/margins/) sein. |

### setMultiplePages(int value) {#setMultiplePages-int}
```
public void setMultiplePages(int value)
```


Für mehrseitige Dokumente ermittelt oder legt fest, wie ein Dokument gedruckt oder gerendert wird, damit es als Heft gebunden werden kann.

 **Examples:** 

Zeigt, wie man Bundsteg‑Ränder festlegt.

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

Zeigt, wie man ein Dokument konfiguriert, das als Buchfalz gedruckt werden kann.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int-Wert. Der Wert muss einer der [MultiplePagesType](../../com.aspose.words/multiplepagestype/) Konstanten sein. |

### setOddAndEvenPagesHeaderFooter(boolean value) {#setOddAndEvenPagesHeaderFooter-boolean}
```
public void setOddAndEvenPagesHeaderFooter(boolean value)
```


True, wenn das Dokument unterschiedliche Kopf‑ und Fußzeilen für ungerade und gerade Seiten hat.

 **Remarks:** 

Hinweis: Das Ändern dieser Eigenschaft wirkt sich auf alle Abschnitte im Dokument aus.

 **Examples:** 

Zeigt, wie man Kopf- und Fußzeilen in einem Dokument mit DocumentBuilder erstellt.

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

Zeigt, wie man gerade Seiten‑Kopf‑/Fußzeilen aktiviert oder deaktiviert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Legt die Ausrichtung der Seite fest.

 **Remarks:** 

Das Ändern von [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int) vertauscht [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) und [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double).

 **Examples:** 

Zeigt, wie man Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument anwendet und zurücksetzt.

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

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Ausrichtung der Seite. Der Wert muss einer der [Orientation](../../com.aspose.words/orientation/) Konstanten sein. |

### setOtherPagesTray(int value) {#setOtherPagesTray-int}
```
public void setOtherPagesTray(int value)
```


Legt das Papierfach (Bin) fest, das für alle Seiten einer Sektion außer der ersten verwendet wird. Der Wert ist implementations- (Drucker-) spezifisch.

 **Examples:** 

Zeigt, wie das Drucken mit verschiedenen Druckerfächern für unterschiedliche Papierformate eingerichtet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Das Papierfach (Bin), das für alle Seiten einer Sektion außer der ersten verwendet wird. |

### setPageHeight(double value) {#setPageHeight-double}
```
public void setPageHeight(double value)
```


Legt die Höhe der Seite in Punkten fest.

 **Examples:** 

Zeigt, wie man ein Bild einfügt und es als Wasserzeichen verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Höhe der Seite in Punkten. |

### setPageNumberStyle(int value) {#setPageNumberStyle-int}
```
public void setPageNumberStyle(int value)
```


Legt das Seitenzahlenformat fest.

 **Examples:** 

Zeigt, wie man die Seitennummerierung in einem Abschnitt einrichtet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Das Seitenzahlenformat. Der Wert muss einer der [NumberStyle](../../com.aspose.words/numberstyle/) Konstanten sein. |

### setPageStartingNumber(int value) {#setPageStartingNumber-int}
```
public void setPageStartingNumber(int value)
```


Legt die Startseitenzahl des Abschnitts fest.

 **Remarks:** 

Die [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) Eigenschaft, wenn sie auf false gesetzt ist, überschreibt die [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) Eigenschaft, sodass die Seitennummerierung vom vorherigen Abschnitt fortgesetzt werden kann.

 **Examples:** 

Zeigt, wie man die Seitennummerierung in einem Abschnitt einrichtet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Startseitenzahl der Sektion. |

### setPageWidth(double value) {#setPageWidth-double}
```
public void setPageWidth(double value)
```


Legt die Breite der Seite in Punkten fest.

 **Examples:** 

Zeigt, wie man ein Bild einfügt und es als Wasserzeichen verwendet.

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

Zeigt, wie man ein schwebendes Bild einfügt und dessen Position und Größe festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Breite der Seite in Punkten. |

### setPaperSize(int value) {#setPaperSize-int}
```
public void setPaperSize(int value)
```


Legt die Papiergröße fest.

 **Remarks:** 

Das Setzen dieser Eigenschaft aktualisiert die Werte von [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) und [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double). Das Setzen dieses Werts auf [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) ändert die bestehenden Werte nicht.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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

Zeigt, wie man Seitengrößen festlegt.

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

Zeigt, wie man die Papiergröße von JisB4 oder JisB5 festlegt.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Papiergröße. Der Wert muss einer der [PaperSize](../../com.aspose.words/papersize/) Konstanten sein. |

### setRestartPageNumbering(boolean value) {#setRestartPageNumbering-boolean}
```
public void setRestartPageNumbering(boolean value)
```


True, wenn die Seitennummerierung am Anfang des Abschnitts neu beginnt.

 **Remarks:** 

Wenn sie auf false gesetzt ist, überschreibt die [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) Eigenschaft die [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) Eigenschaft, sodass die Seitennummerierung vom vorherigen Abschnitt fortgesetzt werden kann.

 **Examples:** 

Zeigt, wie man die Seitennummerierung in einem Abschnitt einrichtet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setRightMargin(double value) {#setRightMargin-double}
```
public void setRightMargin(double value)
```


Legt den Abstand (in Punkten) zwischen dem rechten Rand der Seite und der rechten Begrenzung des Fließtextes fest.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Abstand (in Punkten) zwischen dem rechten Rand der Seite und der rechten Begrenzung des Fließtextes. |

### setRtlGutter(boolean value) {#setRtlGutter-boolean}
```
public void setRtlGutter(boolean value)
```


Legt fest, ob Microsoft Word für den Abschnitt Ränder verwendet, basierend auf einer Rechts-nach-Links- oder Links-nach-Rechts-Sprache.

 **Examples:** 

Zeigt, wie man Bundsteg‑Ränder festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob Microsoft Word für die Sektion Gutter basierend auf einer Rechts-nach-Links- oder einer Links-nach-Rechts-Sprache verwendet. |

### setSectionStart(int value) {#setSectionStart-int}
```
public void setSectionStart(int value)
```


Legt den Typ des Abschnittsumbruchs für das angegebene Objekt fest.

 **Examples:** 

Zeigt, wie man festlegt, wie ein neuer Abschnitt sich vom vorherigen trennt.

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

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Typ des Abschnittsumbruchs für das angegebene Objekt. Der Wert muss einer der [SectionStart](../../com.aspose.words/sectionstart/) Konstanten sein. |

### setSheetsPerBooklet(int value) {#setSheetsPerBooklet-int}
```
public void setSheetsPerBooklet(int value)
```


Legt die Anzahl der Seiten fest, die in jedes Heft aufgenommen werden.

 **Examples:** 

Zeigt, wie man ein Dokument konfiguriert, das als Buchfalz gedruckt werden kann.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Anzahl der Seiten, die in jedem Heft enthalten sein sollen. |

### setSuppressEndnotes(boolean value) {#setSuppressEndnotes-boolean}
```
public void setSuppressEndnotes(boolean value)
```


True, wenn Endnoten am Ende des nächsten Abschnitts gedruckt werden, der Endnoten nicht unterdrückt. Unterdrückte Endnoten werden vor den Endnoten in diesem Abschnitt gedruckt.

 **Examples:** 

Zeigt, wie man Endnoten am Ende jedes Abschnitts speichert und deren Positionen ändert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setTextOrientation(int value) {#setTextOrientation-int}
```
public void setTextOrientation(int value)
```


Ermöglicht das Festlegen von [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) für die gesamte Seite. Der Standardwert ist [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL)

 **Remarks:** 

Diese Eigenschaft wird nur für die nativen MS‑Word‑Formate DOCX, WML, RTF und DOC unterstützt.

 **Examples:** 

Zeigt, wie die Textausrichtung festgelegt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int-Wert. Der Wert muss einer der [TextOrientation](../../com.aspose.words/textorientation/) Konstanten sein. |

### setTopMargin(double value) {#setTopMargin-double}
```
public void setTopMargin(double value)
```


Legt den Abstand (in Punkten) zwischen dem oberen Rand der Seite und der oberen Begrenzung des Fließtextes fest.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Abstand (in Punkten) zwischen dem oberen Rand der Seite und der oberen Begrenzung des Fließtextes. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Legt die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder Abschnitt fest.

 **Examples:** 

Zeigt, wie man Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument anwendet und zurücksetzt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder einer Sektion. Der Wert muss einer der [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/) Konstanten sein. |

