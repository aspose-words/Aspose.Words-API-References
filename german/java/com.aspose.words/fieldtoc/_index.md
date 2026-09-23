---
title: "FieldToc"
linktitle: "FieldToc"
second_title: "Aspose.Words für Java"
description: "Implementiert das TOC‑Feld in Java."
type: docs
weight: 298
url: /de/java/com.aspose.words/fieldtoc/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldToc extends Field
```

Implementiert das TOC-Feld.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Fields ][Working with Fields].

 **Remarks:** 

Erstellt ein Inhaltsverzeichnis (das auch ein Abbildungsverzeichnis sein kann) mithilfe der durch TC‑Felder angegebenen Einträge, deren Überschriftenebenen und festgelegten Stile und fügt dieses Verzeichnis an dieser Stelle im Dokument ein.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

Zeigt, wie man ein Inhaltsverzeichnis-Feld mit Einträgen unter Verwendung von SEQ-Feldern füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBookmarkName()](#getBookmarkName) | Ermittelt den Namen des Lesezeichens, das den Teil des Dokuments markiert, der zum Erstellen des Verzeichnisses verwendet wird. |
| [getCaptionlessTableOfFiguresLabel()](#getCaptionlessTableOfFiguresLabel) | Ermittelt den Namen des Sequenzidentifikators, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das die Beschriftungsbezeichnung und -nummer nicht enthält. |
| [getCustomStyles()](#getCustomStyles) | Ermittelt eine Liste von Stilen, die nicht zu den integrierten Überschriftenstilen gehören, um sie in das Inhaltsverzeichnis aufzunehmen. |
| [getDisplayResult()](#getDisplayResult) | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [getEnd()](#getEnd) | Liefert den Knoten, der das Feldende darstellt. |
| [getEntryIdentifier()](#getEntryIdentifier) | Ermittelt eine Zeichenkette, die mit den Typidentifikatoren der einzuschließenden TC‑Felder übereinstimmen soll. |
| [getEntryLevelRange()](#getEntryLevelRange) | Ermittelt einen Bereich von Ebenen der Inhaltsverzeichnis‑Einträge, die aufgenommen werden sollen. |
| [getEntrySeparator()](#getEntrySeparator) | Ruft eine Zeichenfolge ab, die einen Eintrag und seine Seitenzahl trennt. |
| [getFieldCode()](#getFieldCode) | Gibt den Text zwischen Feldanfang und Feldtrennzeichen zurück (oder das Feldende, wenn kein Trennzeichen vorhanden ist). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Gibt den Text zwischen Feldanfang und Feldtrennzeichen zurück (oder das Feldende, wenn kein Trennzeichen vorhanden ist). |
| [getFormat()](#getFormat) | Liefert ein [FieldFormat](../../com.aspose.words/fieldformat/)‑Objekt, das typisierten Zugriff auf die Formatierung des Feldes ermöglicht. |
| [getHeadingLevelRange()](#getHeadingLevelRange) | Ruft einen Bereich von Überschriftenebenen ab, die eingeschlossen werden sollen. |
| [getHideInWebLayout()](#getHideInWebLayout) | Ruft ab, ob Tabulator-Führungszeichen und Seitenzahlen in der Weblayout-Ansicht ausgeblendet werden sollen. |
| [getInsertHyperlinks()](#getInsertHyperlinks) | Ruft ab, ob die Einträge des Inhaltsverzeichnisses als Hyperlinks erstellt werden sollen. |
| [getLocaleId()](#getLocaleId) | Liefert die LCID des Feldes. |
| [getPageNumberOmittingLevelRange()](#getPageNumberOmittingLevelRange) | Ruft einen Bereich von Ebenen der Inhaltsverzeichniseinträge ab, für die Seitenzahlen weggelassen werden. |
| [getPrefixedSequenceIdentifier()](#getPrefixedSequenceIdentifier) | Ruft den Bezeichner einer Sequenz ab, für die dem Eintrag der Seitenzahl ein Präfix hinzugefügt werden soll. |
| [getPreserveLineBreaks()](#getPreserveLineBreaks) | Ruft ab, ob Zeilenumbrüche innerhalb von Tabelleneinträgen erhalten bleiben sollen. |
| [getPreserveTabs()](#getPreserveTabs) | Ruft ab, ob Tabulator-Einträge innerhalb von Tabelleneinträgen erhalten bleiben sollen. |
| [getResult()](#getResult) | Ermittelt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [getSeparator()](#getSeparator) | Ermittelt den Knoten, der das Feldtrennzeichen darstellt. |
| [getSequenceSeparator()](#getSequenceSeparator) | Ruft die Zeichenfolge ab, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [getStart()](#getStart) | Ermittelt den Knoten, der den Beginn des Feldes darstellt. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getTableOfFiguresLabel()](#getTableOfFiguresLabel) | Ruft den Namen des Sequenzbezeichners ab, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird. |
| [getType()](#getType) | Ermittelt den Microsoft‑Word‑Feldtyp. |
| [getUseParagraphOutlineLevel()](#getUseParagraphOutlineLevel) | Ruft ab, ob die angewandte Absatzgliederungsebene verwendet werden soll. |
| [isDirty()](#isDirty) | Ermittelt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [isDirty(boolean value)](#isDirty-boolean) | Legt fest, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [isLocked()](#isLocked) | Ermittelt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [isLocked(boolean value)](#isLocked-boolean) | Legt fest, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [remove()](#remove) | Entfernt das Feld aus dem Dokument. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | Legt den Namen des Lesezeichens fest, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wird. |
| [setCaptionlessTableOfFiguresLabel(String value)](#setCaptionlessTableOfFiguresLabel-java.lang.String) | Legt den Namen des Sequenzbezeichners fest, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das die Beschriftungsbezeichnung und -nummer nicht enthält. |
| [setCustomStyles(String value)](#setCustomStyles-java.lang.String) | Legt eine Liste von Formatvorlagen fest, die zusätzlich zu den integrierten Überschriftsformaten im Inhaltsverzeichnis enthalten sein sollen. |
| [setEntryIdentifier(String value)](#setEntryIdentifier-java.lang.String) | Legt eine Zeichenfolge fest, die mit den Typbezeichnern der einzuschließenden TC-Felder übereinstimmen soll. |
| [setEntryLevelRange(String value)](#setEntryLevelRange-java.lang.String) | Legt einen Bereich von Ebenen der Inhaltsverzeichniseinträge fest, die eingeschlossen werden sollen. |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String) | Legt eine Zeichenfolge fest, die einen Eintrag und seine Seitenzahl trennt. |
| [setHeadingLevelRange(String value)](#setHeadingLevelRange-java.lang.String) | Legt einen Bereich von Überschriftenebenen fest, die eingeschlossen werden sollen. |
| [setHideInWebLayout(boolean value)](#setHideInWebLayout-boolean) | Legt fest, ob Tabulator-Führungszeichen und Seitenzahlen in der Weblayout-Ansicht ausgeblendet werden sollen. |
| [setInsertHyperlinks(boolean value)](#setInsertHyperlinks-boolean) | Legt fest, ob die Einträge des Inhaltsverzeichnisses als Hyperlinks erstellt werden sollen. |
| [setLocaleId(int value)](#setLocaleId-int) | Legt die LCID des Feldes fest. |
| [setPageNumberOmittingLevelRange(String value)](#setPageNumberOmittingLevelRange-java.lang.String) | Legt einen Bereich von Ebenen der Inhaltsverzeichniseinträge fest, für die Seitenzahlen weggelassen werden. |
| [setPrefixedSequenceIdentifier(String value)](#setPrefixedSequenceIdentifier-java.lang.String) | Legt den Bezeichner einer Sequenz fest, für die dem Eintrag der Seitenzahl ein Präfix hinzugefügt werden soll. |
| [setPreserveLineBreaks(boolean value)](#setPreserveLineBreaks-boolean) | Legt fest, ob Zeilenumbrüche innerhalb von Tabelleneinträgen erhalten bleiben sollen. |
| [setPreserveTabs(boolean value)](#setPreserveTabs-boolean) | Legt fest, ob Tabulator-Einträge innerhalb von Tabelleneinträgen erhalten bleiben sollen. |
| [setResult(String value)](#setResult-java.lang.String) | Setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String) | Legt die Zeichenfolge fest, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [setTableOfFiguresLabel(String value)](#setTableOfFiguresLabel-java.lang.String) | Legt den Namen des Sequenzbezeichners fest, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird. |
| [setUseParagraphOutlineLevel(boolean value)](#setUseParagraphOutlineLevel-boolean) | Legt fest, ob die angewandte Absatzgliederungsebene verwendet werden soll. |
| [unlink()](#unlink) | Führt das Trennen des Feldes aus. |
| [update()](#update) | Führt die Feldaktualisierung aus. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Führt eine Feldaktualisierung aus. |
| [updatePageNumbers()](#updatePageNumbers) | Aktualisiert die Seitenzahlen für die Elemente in diesem Inhaltsverzeichnis. |
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


Ermittelt den Namen des Lesezeichens, das den Teil des Dokuments markiert, der zum Erstellen des Verzeichnisses verwendet wird.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - Der Name des Lesezeichens, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wird.
### getCaptionlessTableOfFiguresLabel() {#getCaptionlessTableOfFiguresLabel}
```
public String getCaptionlessTableOfFiguresLabel()
```


Ermittelt den Namen des Sequenzidentifikators, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das die Beschriftungsbezeichnung und -nummer nicht enthält.

 **Examples:** 

Zeigt, wie der Name des Sequenzidentifikators festgelegt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldToc fieldToc = (FieldToc)builder.insertField(FieldType.FIELD_TOC, true);
 fieldToc.setCaptionlessTableOfFiguresLabel("Test");

 Assert.assertEquals(" TOC  \\a Test", fieldToc.getFieldCode());
 
```

**Returns:**
java.lang.String - Der Name des Sequenzidentifikators, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird und die Beschriftungsbezeichnung und -nummer nicht enthält.
### getCustomStyles() {#getCustomStyles}
```
public String getCustomStyles()
```


Ermittelt eine Liste von Stilen, die nicht zu den integrierten Überschriftenstilen gehören, um sie in das Inhaltsverzeichnis aufzunehmen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - Eine Liste von Formatvorlagen, die nicht zu den integrierten Überschriftenformaten gehören, und im Inhaltsverzeichnis aufgenommen werden sollen.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Liefert den Text, der das angezeigte Feldresultat darstellt.

 **Remarks:** 

Die Methode [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) muss aufgerufen werden, um den korrekten Wert für die Felder [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) und [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/) zu erhalten.

 **Examples:** 

Zeigt, wie man den tatsächlichen Text ermittelt, den ein Feld im Dokument anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("This document was written by ");
 FieldAuthor fieldAuthor = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);
 fieldAuthor.setAuthorName("John Doe");

 // We can use the DisplayResult property to verify what exact text
 // a field would display in its place in the document.
 Assert.assertEquals("", fieldAuthor.getDisplayResult());

 // Fields do not maintain accurate result values in real-time.
 // To make sure our fields display accurate results at any given time,
 // such as right before a save operation, we need to update them manually.
 fieldAuthor.update();

 Assert.assertEquals("John Doe", fieldAuthor.getDisplayResult());

 doc.save(getArtifactsDir() + "Field.DisplayResult.docx");
 
```

**Returns:**
java.lang.String – Der Text, der das angezeigte Feldresultat darstellt.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Liefert den Knoten, der das Feldende darstellt.

 **Examples:** 

Zeigt, wie man mit einer Sammlung von Feldern arbeitet.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend/) - The node that represents the field end.
### getEntryIdentifier() {#getEntryIdentifier}
```
public String getEntryIdentifier()
```


Ermittelt eine Zeichenkette, die mit den Typidentifikatoren der einzuschließenden TC‑Felder übereinstimmen soll.

 **Examples:** 

Zeigt, wie man ein TOC‑Feld einfügt und filtert, welche TC‑Felder als Einträge erscheinen.

```

 public void fieldTocEntryIdentifier() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOC field, which will compile all TC fields into a table of contents.
     FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
     fieldToc.setEntryIdentifier("A");
     fieldToc.setEntryLevelRange("1-3");

     Assert.assertEquals(" TOC  \\f A \\l 1-3", fieldToc.getFieldCode());

     // These two entries will appear in the table.
     builder.insertBreak(BreakType.PAGE_BREAK);
     insertTocEntry(builder, "TC field 1", "A", "1");
     insertTocEntry(builder, "TC field 2", "A", "2");

     Assert.assertEquals(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.getRange().getFields().get(1).getFieldCode());

     // This entry will be omitted from the table because it has a different type from "A".
     insertTocEntry(builder, "TC field 3", "B", "1");

     // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
     insertTocEntry(builder, "TC field 4", "A", "5");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TC.docx");
 }

 /// 
 /// Use a document builder to insert a TC field.
 /// 
 public void insertTocEntry(final DocumentBuilder builder, final String text, final String typeIdentifier, final String entryLevel) throws Exception {
     FieldTC fieldTc = (FieldTC) builder.insertField(FieldType.FIELD_TOC_ENTRY, true);
     fieldTc.setOmitPageNumber(true);
     fieldTc.setText(text);
     fieldTc.setTypeIdentifier(typeIdentifier);
     fieldTc.setEntryLevel(entryLevel);
 }
 
```

**Returns:**
java.lang.String - Eine Zeichenkette, die mit den Typidentifikatoren der einzuschließenden TC-Felder übereinstimmen soll.
### getEntryLevelRange() {#getEntryLevelRange}
```
public String getEntryLevelRange()
```


Ermittelt einen Bereich von Ebenen der Inhaltsverzeichnis‑Einträge, die aufgenommen werden sollen.

 **Examples:** 

Zeigt, wie man ein TOC‑Feld einfügt und filtert, welche TC‑Felder als Einträge erscheinen.

```

 public void fieldTocEntryIdentifier() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOC field, which will compile all TC fields into a table of contents.
     FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
     fieldToc.setEntryIdentifier("A");
     fieldToc.setEntryLevelRange("1-3");

     Assert.assertEquals(" TOC  \\f A \\l 1-3", fieldToc.getFieldCode());

     // These two entries will appear in the table.
     builder.insertBreak(BreakType.PAGE_BREAK);
     insertTocEntry(builder, "TC field 1", "A", "1");
     insertTocEntry(builder, "TC field 2", "A", "2");

     Assert.assertEquals(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.getRange().getFields().get(1).getFieldCode());

     // This entry will be omitted from the table because it has a different type from "A".
     insertTocEntry(builder, "TC field 3", "B", "1");

     // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
     insertTocEntry(builder, "TC field 4", "A", "5");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TC.docx");
 }

 /// 
 /// Use a document builder to insert a TC field.
 /// 
 public void insertTocEntry(final DocumentBuilder builder, final String text, final String typeIdentifier, final String entryLevel) throws Exception {
     FieldTC fieldTc = (FieldTC) builder.insertField(FieldType.FIELD_TOC_ENTRY, true);
     fieldTc.setOmitPageNumber(true);
     fieldTc.setText(text);
     fieldTc.setTypeIdentifier(typeIdentifier);
     fieldTc.setEntryLevel(entryLevel);
 }
 
```

**Returns:**
java.lang.String - Ein Bereich von Ebenen der Inhaltsverzeichniseinträge, die aufgenommen werden sollen.
### getEntrySeparator() {#getEntrySeparator}
```
public String getEntrySeparator()
```


Ruft eine Zeichenfolge ab, die einen Eintrag und seine Seitenzahl trennt.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - Eine Zeichenfolge, die einen Eintrag und seine Seitenzahl trennt.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten.

 **Examples:** 

Zeigt, wie man ein Feld mithilfe eines Feldcodes in ein Dokument einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Zeigt, wie man den Feldcode eines Feldes erhält.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Gibt den Text zwischen Feldanfang und Feldtrennzeichen zurück (oder das Feldende, wenn kein Trennzeichen vorhanden ist).

 **Examples:** 

Zeigt, wie man den Feldcode eines Feldes erhält.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true  wenn Kindfeldcodes eingeschlossen werden sollen. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Liefert ein [FieldFormat](../../com.aspose.words/fieldformat/)‑Objekt, das typisierten Zugriff auf die Formatierung des Feldes ermöglicht.

 **Examples:** 

Zeigt, wie man Feldresultate formatiert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat/) - A [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.
### getHeadingLevelRange() {#getHeadingLevelRange}
```
public String getHeadingLevelRange()
```


Ruft einen Bereich von Überschriftenebenen ab, die eingeschlossen werden sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - Ein Bereich von Überschriftsebenen, die aufgenommen werden sollen.
### getHideInWebLayout() {#getHideInWebLayout}
```
public boolean getHideInWebLayout()
```


Ruft ab, ob Tabulator-Führungszeichen und Seitenzahlen in der Weblayout-Ansicht ausgeblendet werden sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - Ob Tab-Führungszeichen und Seitenzahlen in der Weblayout-Ansicht ausgeblendet werden sollen.
### getInsertHyperlinks() {#getInsertHyperlinks}
```
public boolean getInsertHyperlinks()
```


Ruft ab, ob die Einträge des Inhaltsverzeichnisses als Hyperlinks erstellt werden sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - Ob die Einträge des Inhaltsverzeichnisses als Hyperlinks dargestellt werden sollen.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Liefert die LCID des Feldes.

 **Examples:** 

Zeigt, wie man ein Feld einfügt und mit seiner Gebietseinstellung arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Returns:**
int - Die LCID des Feldes.
### getPageNumberOmittingLevelRange() {#getPageNumberOmittingLevelRange}
```
public String getPageNumberOmittingLevelRange()
```


Ruft einen Bereich von Ebenen der Inhaltsverzeichniseinträge ab, für die Seitenzahlen weggelassen werden.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - Ein Bereich von Ebenen der Inhaltsverzeichniseinträge, aus denen Seitenzahlen weggelassen werden sollen.
### getPrefixedSequenceIdentifier() {#getPrefixedSequenceIdentifier}
```
public String getPrefixedSequenceIdentifier()
```


Ruft den Bezeichner einer Sequenz ab, für die dem Eintrag der Seitenzahl ein Präfix hinzugefügt werden soll.

 **Examples:** 

Zeigt, wie man ein Inhaltsverzeichnis-Feld mit Einträgen unter Verwendung von SEQ-Feldern füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Returns:**
java.lang.String - Der Identifikator einer Sequenz, für die dem Eintrag eine Präfix zur Seitenzahl hinzugefügt werden soll.
### getPreserveLineBreaks() {#getPreserveLineBreaks}
```
public boolean getPreserveLineBreaks()
```


Ruft ab, ob Zeilenumbrüche innerhalb von Tabelleneinträgen erhalten bleiben sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - Ob Zeilenumbrüche innerhalb von Tabelleneinträgen erhalten bleiben sollen.
### getPreserveTabs() {#getPreserveTabs}
```
public boolean getPreserveTabs()
```


Ruft ab, ob Tabulator-Einträge innerhalb von Tabelleneinträgen erhalten bleiben sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - Ob Tabulatoren innerhalb von Tabelleneinträgen erhalten bleiben sollen.
### getResult() {#getResult}
```
public String getResult()
```


Ermittelt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt.

 **Examples:** 

Zeigt, wie man ein Feld mithilfe eines Feldcodes in ein Dokument einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann  null  sein.

 **Examples:** 

Zeigt, wie man mit einer Sammlung von Feldern arbeitet.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator/) - The node that represents the field separator.
### getSequenceSeparator() {#getSequenceSeparator}
```
public String getSequenceSeparator()
```


Ruft die Zeichenfolge ab, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen.

 **Examples:** 

Zeigt, wie man ein Inhaltsverzeichnis-Feld mit Einträgen unter Verwendung von SEQ-Feldern füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Returns:**
java.lang.String - Die Zeichenfolge, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Ermittelt den Knoten, der den Beginn des Feldes darstellt.

 **Examples:** 

Zeigt, wie man mit einer Sammlung von Feldern arbeitet.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart/) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getTableOfFiguresLabel() {#getTableOfFiguresLabel}
```
public String getTableOfFiguresLabel()
```


Ruft den Namen des Sequenzbezeichners ab, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird.

 **Examples:** 

Zeigt, wie man ein Inhaltsverzeichnis-Feld mit Einträgen unter Verwendung von SEQ-Feldern füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Returns:**
java.lang.String - Der Name des Sequenzidentifikators, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird.
### getType() {#getType}
```
public int getType()
```


Ermittelt den Microsoft‑Word‑Feldtyp.

 **Examples:** 

Zeigt, wie man ein Feld mithilfe eines Feldcodes in ein Dokument einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - Der Microsoft‑Word‑Feldtyp. Der zurückgegebene Wert ist einer der [FieldType](../../com.aspose.words/fieldtype/) Konstanten.
### getUseParagraphOutlineLevel() {#getUseParagraphOutlineLevel}
```
public boolean getUseParagraphOutlineLevel()
```


Ruft ab, ob die angewandte Absatzgliederungsebene verwendet werden soll.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - Ob die angewandte Absatzgliederungsebene verwendet werden soll.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Ermittelt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist.

 **Examples:** 

Zeigt, wie man die spezielle Eigenschaft zum Aktualisieren des Feldergebnisses verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Returns:**
boolean - Ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Legt fest, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist.

 **Examples:** 

Zeigt, wie man die spezielle Eigenschaft zum Aktualisieren des Feldergebnisses verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Ermittelt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen).

 **Examples:** 

Zeigt, wie man mit einem FieldStart‑Knoten arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Returns:**
boolean - Ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Legt fest, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen).

 **Examples:** 

Zeigt, wie man mit einem FieldStart‑Knoten arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |

### remove() {#remove}
```
public Node remove()
```


Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Feldende das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man Felder aus einer Feldsammlung entfernt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
 builder.insertField(" TIME ");
 builder.insertField(" REVNUM ");
 builder.insertField(" AUTHOR  \"John Doe\" ");
 builder.insertField(" SUBJECT \"My Subject\" ");
 builder.insertField(" QUOTE \"Hello world!\" ");
 doc.updateFields();

 FieldCollection fields = doc.getRange().getFields();

 Assert.assertEquals(6, fields.getCount());

 // Below are four ways of removing fields from a field collection.
 // 1 -  Get a field to remove itself:
 fields.get(0).remove();
 Assert.assertEquals(5, fields.getCount());

 // 2 -  Get the collection to remove a field that we pass to its removal method:
 Field lastField = fields.get(3);
 fields.remove(lastField);
 Assert.assertEquals(4, fields.getCount());

 // 3 -  Remove a field from a collection at an index:
 fields.removeAt(2);
 Assert.assertEquals(3, fields.getCount());

 // 4 -  Remove all the fields from the collection at once:
 fields.clear();
 Assert.assertEquals(0, fields.getCount());
 
```

Zeigt, wie PRIVATE‑Felder verarbeitet werden.

```

 public void fieldPrivate() throws Exception {
     // Open a Corel WordPerfect document which we have converted to .docx format.
     Document doc = new Document(getMyDir() + "Field sample - PRIVATE.docx");

     // WordPerfect 5.x/6.x documents like the one we have loaded may contain PRIVATE fields.
     // Microsoft Word preserves PRIVATE fields during load/save operations,
     // but provides no functionality for them.
     FieldPrivate field = (FieldPrivate) doc.getRange().getFields().get(0);

     Assert.assertEquals(" PRIVATE \"My value\" ", field.getFieldCode());
     Assert.assertEquals(FieldType.FIELD_PRIVATE, field.getType());

     // We can also insert PRIVATE fields using a document builder.
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(FieldType.FIELD_PRIVATE, true);

     // These fields are not a viable way of protecting sensitive information.
     // Unless backward compatibility with older versions of WordPerfect is essential,
     // we can safely remove these fields. We can do this using a DocumentVisiitor implementation.
     Assert.assertEquals(2, doc.getRange().getFields().getCount());

     FieldPrivateRemover remover = new FieldPrivateRemover();
     doc.accept(remover);

     Assert.assertEquals(remover.getFieldsRemovedCount(), 2);
     Assert.assertEquals(doc.getRange().getFields().getCount(), 0);
 }

 /// 
 /// Removes all encountered PRIVATE fields.
 /// 
 public static class FieldPrivateRemover extends DocumentVisitor {
     public FieldPrivateRemover() {
         mFieldsRemovedCount = 0;
     }

     public int getFieldsRemovedCount() {
         return mFieldsRemovedCount;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// If the node belongs to a PRIVATE field, the entire field is removed.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) throws Exception {
         if (fieldEnd.getFieldType() == FieldType.FIELD_PRIVATE) {
             fieldEnd.getField().remove();
             mFieldsRemovedCount++;
         }

         return VisitorAction.CONTINUE;
     }

     private int mFieldsRemovedCount;
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/)
### setBookmarkName(String value) {#setBookmarkName-java.lang.String}
```
public void setBookmarkName(String value)
```


Legt den Namen des Lesezeichens fest, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wird.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name des Lesezeichens, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wird. |

### setCaptionlessTableOfFiguresLabel(String value) {#setCaptionlessTableOfFiguresLabel-java.lang.String}
```
public void setCaptionlessTableOfFiguresLabel(String value)
```


Legt den Namen des Sequenzbezeichners fest, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das die Beschriftungsbezeichnung und -nummer nicht enthält.

 **Examples:** 

Zeigt, wie der Name des Sequenzidentifikators festgelegt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldToc fieldToc = (FieldToc)builder.insertField(FieldType.FIELD_TOC, true);
 fieldToc.setCaptionlessTableOfFiguresLabel("Test");

 Assert.assertEquals(" TOC  \\a Test", fieldToc.getFieldCode());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name des Sequenzidentifikators, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird und die Beschriftungsbezeichnung und -nummer nicht enthält. |

### setCustomStyles(String value) {#setCustomStyles-java.lang.String}
```
public void setCustomStyles(String value)
```


Legt eine Liste von Formatvorlagen fest, die zusätzlich zu den integrierten Überschriftsformaten im Inhaltsverzeichnis enthalten sein sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Eine Liste von Formatvorlagen, die nicht zu den integrierten Überschriftenformaten gehören, und im Inhaltsverzeichnis aufgenommen werden sollen. |

### setEntryIdentifier(String value) {#setEntryIdentifier-java.lang.String}
```
public void setEntryIdentifier(String value)
```


Legt eine Zeichenfolge fest, die mit den Typbezeichnern der einzuschließenden TC-Felder übereinstimmen soll.

 **Examples:** 

Zeigt, wie man ein TOC‑Feld einfügt und filtert, welche TC‑Felder als Einträge erscheinen.

```

 public void fieldTocEntryIdentifier() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOC field, which will compile all TC fields into a table of contents.
     FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
     fieldToc.setEntryIdentifier("A");
     fieldToc.setEntryLevelRange("1-3");

     Assert.assertEquals(" TOC  \\f A \\l 1-3", fieldToc.getFieldCode());

     // These two entries will appear in the table.
     builder.insertBreak(BreakType.PAGE_BREAK);
     insertTocEntry(builder, "TC field 1", "A", "1");
     insertTocEntry(builder, "TC field 2", "A", "2");

     Assert.assertEquals(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.getRange().getFields().get(1).getFieldCode());

     // This entry will be omitted from the table because it has a different type from "A".
     insertTocEntry(builder, "TC field 3", "B", "1");

     // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
     insertTocEntry(builder, "TC field 4", "A", "5");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TC.docx");
 }

 /// 
 /// Use a document builder to insert a TC field.
 /// 
 public void insertTocEntry(final DocumentBuilder builder, final String text, final String typeIdentifier, final String entryLevel) throws Exception {
     FieldTC fieldTc = (FieldTC) builder.insertField(FieldType.FIELD_TOC_ENTRY, true);
     fieldTc.setOmitPageNumber(true);
     fieldTc.setText(text);
     fieldTc.setTypeIdentifier(typeIdentifier);
     fieldTc.setEntryLevel(entryLevel);
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Eine Zeichenkette, die mit den Typidentifikatoren der einzuschließenden TC-Felder übereinstimmen soll. |

### setEntryLevelRange(String value) {#setEntryLevelRange-java.lang.String}
```
public void setEntryLevelRange(String value)
```


Legt einen Bereich von Ebenen der Inhaltsverzeichniseinträge fest, die eingeschlossen werden sollen.

 **Examples:** 

Zeigt, wie man ein TOC‑Feld einfügt und filtert, welche TC‑Felder als Einträge erscheinen.

```

 public void fieldTocEntryIdentifier() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOC field, which will compile all TC fields into a table of contents.
     FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
     fieldToc.setEntryIdentifier("A");
     fieldToc.setEntryLevelRange("1-3");

     Assert.assertEquals(" TOC  \\f A \\l 1-3", fieldToc.getFieldCode());

     // These two entries will appear in the table.
     builder.insertBreak(BreakType.PAGE_BREAK);
     insertTocEntry(builder, "TC field 1", "A", "1");
     insertTocEntry(builder, "TC field 2", "A", "2");

     Assert.assertEquals(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.getRange().getFields().get(1).getFieldCode());

     // This entry will be omitted from the table because it has a different type from "A".
     insertTocEntry(builder, "TC field 3", "B", "1");

     // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
     insertTocEntry(builder, "TC field 4", "A", "5");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TC.docx");
 }

 /// 
 /// Use a document builder to insert a TC field.
 /// 
 public void insertTocEntry(final DocumentBuilder builder, final String text, final String typeIdentifier, final String entryLevel) throws Exception {
     FieldTC fieldTc = (FieldTC) builder.insertField(FieldType.FIELD_TOC_ENTRY, true);
     fieldTc.setOmitPageNumber(true);
     fieldTc.setText(text);
     fieldTc.setTypeIdentifier(typeIdentifier);
     fieldTc.setEntryLevel(entryLevel);
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein Bereich von Ebenen der Inhaltsverzeichniseinträge, die aufgenommen werden sollen. |

### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String}
```
public void setEntrySeparator(String value)
```


Legt eine Zeichenfolge fest, die einen Eintrag und seine Seitenzahl trennt.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Eine Zeichenfolge, die einen Eintrag und seine Seitenzahl trennt. |

### setHeadingLevelRange(String value) {#setHeadingLevelRange-java.lang.String}
```
public void setHeadingLevelRange(String value)
```


Legt einen Bereich von Überschriftenebenen fest, die eingeschlossen werden sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein Bereich von Überschriftsebenen, die aufgenommen werden sollen. |

### setHideInWebLayout(boolean value) {#setHideInWebLayout-boolean}
```
public void setHideInWebLayout(boolean value)
```


Legt fest, ob Tabulator-Führungszeichen und Seitenzahlen in der Weblayout-Ansicht ausgeblendet werden sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob Tab-Führungszeichen und Seitenzahlen in der Weblayout-Ansicht ausgeblendet werden sollen. |

### setInsertHyperlinks(boolean value) {#setInsertHyperlinks-boolean}
```
public void setInsertHyperlinks(boolean value)
```


Legt fest, ob die Einträge des Inhaltsverzeichnisses als Hyperlinks erstellt werden sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob die Einträge des Inhaltsverzeichnisses als Hyperlinks dargestellt werden sollen. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Legt die LCID des Feldes fest.

 **Examples:** 

Zeigt, wie man ein Feld einfügt und mit seiner Gebietseinstellung arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die LCID des Feldes. |

### setPageNumberOmittingLevelRange(String value) {#setPageNumberOmittingLevelRange-java.lang.String}
```
public void setPageNumberOmittingLevelRange(String value)
```


Legt einen Bereich von Ebenen der Inhaltsverzeichniseinträge fest, für die Seitenzahlen weggelassen werden.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein Bereich von Ebenen der Inhaltsverzeichniseinträge, aus denen Seitenzahlen weggelassen werden sollen. |

### setPrefixedSequenceIdentifier(String value) {#setPrefixedSequenceIdentifier-java.lang.String}
```
public void setPrefixedSequenceIdentifier(String value)
```


Legt den Bezeichner einer Sequenz fest, für die dem Eintrag der Seitenzahl ein Präfix hinzugefügt werden soll.

 **Examples:** 

Zeigt, wie man ein Inhaltsverzeichnis-Feld mit Einträgen unter Verwendung von SEQ-Feldern füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Identifikator einer Sequenz, für die dem Eintrag eine Präfix zur Seitenzahl hinzugefügt werden soll. |

### setPreserveLineBreaks(boolean value) {#setPreserveLineBreaks-boolean}
```
public void setPreserveLineBreaks(boolean value)
```


Legt fest, ob Zeilenumbrüche innerhalb von Tabelleneinträgen erhalten bleiben sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob Zeilenumbrüche innerhalb von Tabelleneinträgen erhalten bleiben sollen. |

### setPreserveTabs(boolean value) {#setPreserveTabs-boolean}
```
public void setPreserveTabs(boolean value)
```


Legt fest, ob Tabulator-Einträge innerhalb von Tabelleneinträgen erhalten bleiben sollen.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob Tabulatoren innerhalb von Tabelleneinträgen erhalten bleiben sollen. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt.

 **Examples:** 

Zeigt, wie man ein Feld mithilfe eines Feldcodes in ein Dokument einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String}
```
public void setSequenceSeparator(String value)
```


Legt die Zeichenfolge fest, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen.

 **Examples:** 

Zeigt, wie man ein Inhaltsverzeichnis-Feld mit Einträgen unter Verwendung von SEQ-Feldern füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Zeichenfolge, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |

### setTableOfFiguresLabel(String value) {#setTableOfFiguresLabel-java.lang.String}
```
public void setTableOfFiguresLabel(String value)
```


Legt den Namen des Sequenzbezeichners fest, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird.

 **Examples:** 

Zeigt, wie man ein Inhaltsverzeichnis-Feld mit Einträgen unter Verwendung von SEQ-Feldern füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name des Sequenzidentifikators, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird. |

### setUseParagraphOutlineLevel(boolean value) {#setUseParagraphOutlineLevel-boolean}
```
public void setUseParagraphOutlineLevel(boolean value)
```


Legt fest, ob die angewandte Absatzgliederungsebene verwendet werden soll.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob die angewandte Absatzgliederungsebene verwendet werden soll. |

### unlink() {#unlink}
```
public boolean unlink()
```


Führt das Trennen des Feldes aus.

 **Remarks:** 

Ersetzt das Feld durch sein zuletzt berechnetes Ergebnis.

Einige Felder, wie XE‑(Indexeintrag‑)Felder und SEQ‑(Sequenz‑)Felder, können nicht entkoppelt werden.

 **Examples:** 

Zeigt, wie man ein Feld entkoppelt.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  wenn das Feld entkoppelt wurde, sonst  false .
### update() {#update}
```
public void update()
```


Führt die Feldaktualisierung durch. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird.

 **Examples:** 

Zeigt, wie man ein Feld in ein Dokument einfügt, indem man FieldType verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
 // In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 builder.write("This document was written by ");
 builder.insertField(FieldType.FIELD_AUTHOR, updateInsertedFieldsImmediately);

 builder.insertParagraph();
 builder.write("\nThis is page ");
 builder.insertField(FieldType.FIELD_PAGE, updateInsertedFieldsImmediately);

 Assert.assertEquals(" AUTHOR ", doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(" PAGE ", doc.getRange().getFields().get(1).getFieldCode());

 if (updateInsertedFieldsImmediately) {
     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 } else {
     Assert.assertEquals("", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("", doc.getRange().getFields().get(1).getResult());

     // We will need to update these fields using the update methods manually.
     doc.getRange().getFields().get(0).update();

     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());

     doc.updateFields();

     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 }
 
```

Zeigt, wie man Feldresultate formatiert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

### update(boolean ignoreMergeFormat) {#update-boolean}
```
public void update(boolean ignoreMergeFormat)
```


Führt eine Feldaktualisierung durch. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird.

 **Examples:** 

Zeigt, wie man INCLUDEPICTURE‑Felder beim Laden eines Dokuments beibehält oder verwirft.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ignoreMergeFormat | boolean | Wenn true, wird die direkte Feldresultatformatierung verworfen, unabhängig vom MERGEFORMAT‑Schalter; andernfalls wird ein normales Update durchgeführt. |

### updatePageNumbers() {#updatePageNumbers}
```
public boolean updatePageNumbers()
```


Aktualisiert die Seitenzahlen für die Elemente in diesem Inhaltsverzeichnis.

 **Examples:** 

Zeigt, wie ein TOC eingefügt und mit Einträgen basierend auf Überschriftsstilen gefüllt wird.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean -  true  wenn die Operation erfolgreich ist. Wenn ein zugehöriges TOC-Lesezeichen entfernt wurde, wird  false  zurückgegeben.
