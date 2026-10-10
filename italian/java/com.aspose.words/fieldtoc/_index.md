---
title: "FieldToc"
linktitle: "FieldToc"
second_title: "Aspose.Words per Java"
description: "Implementa il campo TOC in Java."
type: docs
weight: 298
url: /it/java/com.aspose.words/fieldtoc/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldToc extends Field
```

Implementa il campo TOC.

Per saperne di più, visita l'articolo di documentazione [ Working with Fields ][Working with Fields].

 **Remarks:** 

Crea un indice (che può anche essere un indice delle figure) utilizzando le voci specificate dai campi TC, i loro livelli di intestazione e gli stili specificati, e inserisce tale indice in questo punto del documento.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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

Mostra come popolare un campo TOC con voci usando i campi SEQ.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getBookmarkName()](#getBookmarkName) | Ottiene il nome del segnalibro che indica la parte del documento utilizzata per costruire la tabella. |
| [getCaptionlessTableOfFiguresLabel()](#getCaptionlessTableOfFiguresLabel) | Ottiene il nome dell'identificatore di sequenza usato quando si crea un indice delle figure che non include l'etichetta e il numero della didascalia. |
| [getCustomStyles()](#getCustomStyles) | Ottiene un elenco di stili diversi dagli stili di intestazione predefiniti da includere nel sommario. |
| [getDisplayResult()](#getDisplayResult) | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [getEnd()](#getEnd) | Ottiene il nodo che rappresenta la fine del campo. |
| [getEntryIdentifier()](#getEntryIdentifier) | Ottiene una stringa che deve corrispondere agli identificatori di tipo dei campi TC inclusi. |
| [getEntryLevelRange()](#getEntryLevelRange) | Ottiene un intervallo di livelli delle voci del sommario da includere. |
| [getEntrySeparator()](#getEntrySeparator) | Ottiene una sequenza di caratteri che separa una voce dal suo numero di pagina. |
| [getFieldCode()](#getFieldCode) | Restituisce il testo compreso tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Restituisce il testo compreso tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore). |
| [getFormat()](#getFormat) | Ottiene un oggetto [FieldFormat](../../com.aspose.words/fieldformat/) che fornisce accesso tipizzato alla formattazione del campo. |
| [getHeadingLevelRange()](#getHeadingLevelRange) | Ottiene un intervallo di livelli di intestazione da includere. |
| [getHideInWebLayout()](#getHideInWebLayout) | Ottiene se nascondere il leader di tabulazione e i numeri di pagina nella visualizzazione layout Web. |
| [getInsertHyperlinks()](#getInsertHyperlinks) | Ottiene se rendere le voci del sommario dei collegamenti ipertestuali. |
| [getLocaleId()](#getLocaleId) | Ottiene il LCID del campo. |
| [getPageNumberOmittingLevelRange()](#getPageNumberOmittingLevelRange) | Ottiene un intervallo di livelli delle voci del sommario da cui omettere i numeri di pagina. |
| [getPrefixedSequenceIdentifier()](#getPrefixedSequenceIdentifier) | Ottiene l'identificatore di una sequenza per la quale deve essere aggiunto un prefisso al numero di pagina della voce. |
| [getPreserveLineBreaks()](#getPreserveLineBreaks) | Ottiene se preservare i caratteri di nuova riga all'interno delle voci della tabella. |
| [getPreserveTabs()](#getPreserveTabs) | Ottiene se preservare le voci di tabulazione all'interno delle voci della tabella. |
| [getResult()](#getResult) | Ottiene il testo compreso tra il separatore del campo e la fine del campo. |
| [getSeparator()](#getSeparator) | Ottiene il nodo che rappresenta il separatore di campo. |
| [getSequenceSeparator()](#getSequenceSeparator) | Ottiene la sequenza di caratteri utilizzata per separare i numeri di sequenza dai numeri di pagina. |
| [getStart()](#getStart) | Ottiene il nodo che rappresenta l'inizio del campo. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getTableOfFiguresLabel()](#getTableOfFiguresLabel) | Ottiene il nome dell'identificatore di sequenza utilizzato durante la creazione di un indice delle figure. |
| [getType()](#getType) | Ottiene il tipo di campo di Microsoft Word. |
| [getUseParagraphOutlineLevel()](#getUseParagraphOutlineLevel) | Ottiene se utilizzare il livello di contorno del paragrafo applicato. |
| [isDirty()](#isDirty) | Ottiene se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [isDirty(boolean value)](#isDirty-boolean) | Imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [isLocked()](#isLocked) | Ottiene se il campo è bloccato (non deve ricalcolare il suo risultato). |
| [isLocked(boolean value)](#isLocked-boolean) | Imposta se il campo è bloccato (non deve ricalcolare il suo risultato). |
| [remove()](#remove) | Rimuove il campo dal documento. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | Imposta il nome del segnalibro che indica la parte del documento utilizzata per costruire la tabella. |
| [setCaptionlessTableOfFiguresLabel(String value)](#setCaptionlessTableOfFiguresLabel-java.lang.String) | Imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di un indice delle figure che non include l'etichetta e il numero della didascalia. |
| [setCustomStyles(String value)](#setCustomStyles-java.lang.String) | Imposta un elenco di stili diversi dagli stili di intestazione predefiniti da includere nel sommario. |
| [setEntryIdentifier(String value)](#setEntryIdentifier-java.lang.String) | Imposta una stringa che deve corrispondere agli identificatori di tipo dei campi TC inclusi. |
| [setEntryLevelRange(String value)](#setEntryLevelRange-java.lang.String) | Imposta un intervallo di livelli delle voci del sommario da includere. |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String) | Imposta una sequenza di caratteri che separa una voce dal suo numero di pagina. |
| [setHeadingLevelRange(String value)](#setHeadingLevelRange-java.lang.String) | Imposta un intervallo di livelli di intestazione da includere. |
| [setHideInWebLayout(boolean value)](#setHideInWebLayout-boolean) | Imposta se nascondere il leader di tabulazione e i numeri di pagina nella visualizzazione layout Web. |
| [setInsertHyperlinks(boolean value)](#setInsertHyperlinks-boolean) | Imposta se rendere le voci del sommario dei collegamenti ipertestuali. |
| [setLocaleId(int value)](#setLocaleId-int) | Imposta il LCID del campo. |
| [setPageNumberOmittingLevelRange(String value)](#setPageNumberOmittingLevelRange-java.lang.String) | Imposta un intervallo di livelli delle voci del sommario da cui omettere i numeri di pagina. |
| [setPrefixedSequenceIdentifier(String value)](#setPrefixedSequenceIdentifier-java.lang.String) | Imposta l'identificatore di una sequenza per la quale deve essere aggiunto un prefisso al numero di pagina della voce. |
| [setPreserveLineBreaks(boolean value)](#setPreserveLineBreaks-boolean) | Imposta se preservare i caratteri di nuova riga all'interno delle voci della tabella. |
| [setPreserveTabs(boolean value)](#setPreserveTabs-boolean) | Imposta se preservare le voci di tabulazione all'interno delle voci della tabella. |
| [setResult(String value)](#setResult-java.lang.String) | Imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String) | Imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza dai numeri di pagina. |
| [setTableOfFiguresLabel(String value)](#setTableOfFiguresLabel-java.lang.String) | Imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella delle figure. |
| [setUseParagraphOutlineLevel(boolean value)](#setUseParagraphOutlineLevel-boolean) | Imposta se utilizzare il livello di contorno del paragrafo applicato. |
| [unlink()](#unlink) | Esegue lo scollegamento del campo. |
| [update()](#update) | Esegue l'aggiornamento del campo. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Esegue un aggiornamento del campo. |
| [updatePageNumbers()](#updatePageNumbers) | Aggiorna i numeri di pagina per gli elementi di questo indice. |
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


Ottiene il nome del segnalibro che indica la parte del documento utilizzata per costruire la tabella.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
java.lang.String - Il nome del segnalibro che indica la parte del documento utilizzata per costruire la tabella.
### getCaptionlessTableOfFiguresLabel() {#getCaptionlessTableOfFiguresLabel}
```
public String getCaptionlessTableOfFiguresLabel()
```


Ottiene il nome dell'identificatore di sequenza usato quando si crea un indice delle figure che non include l'etichetta e il numero della didascalia.

 **Examples:** 

Mostra come impostare il nome dell'identificatore di sequenza.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldToc fieldToc = (FieldToc)builder.insertField(FieldType.FIELD_TOC, true);
 fieldToc.setCaptionlessTableOfFiguresLabel("Test");

 Assert.assertEquals(" TOC  \\a Test", fieldToc.getFieldCode());
 
```

**Returns:**
java.lang.String - Il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella delle figure che non include l'etichetta e il numero della didascalia.
### getCustomStyles() {#getCustomStyles}
```
public String getCustomStyles()
```


Ottiene un elenco di stili diversi dagli stili di intestazione predefiniti da includere nel sommario.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
java.lang.String - Un elenco di stili diversi dagli stili di intestazione predefiniti da includere nell'indice.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Ottiene il testo che rappresenta il risultato del campo visualizzato.

 **Remarks:** 

Il metodo [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) deve essere chiamato per ottenere il valore corretto per i campi [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) e [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/).

 **Examples:** 

Mostra come ottenere il testo reale che un campo visualizza nel documento.

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
java.lang.String - Il testo che rappresenta il risultato del campo visualizzato.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Ottiene il nodo che rappresenta la fine del campo.

 **Examples:** 

Mostra come lavorare con una raccolta di campi.

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


Ottiene una stringa che deve corrispondere agli identificatori di tipo dei campi TC inclusi.

 **Examples:** 

Mostra come inserire un campo TOC e filtrare quali campi TC diventano voci.

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
java.lang.String - Una stringa che dovrebbe corrispondere agli identificatori di tipo dei campi TC da includere.
### getEntryLevelRange() {#getEntryLevelRange}
```
public String getEntryLevelRange()
```


Ottiene un intervallo di livelli delle voci del sommario da includere.

 **Examples:** 

Mostra come inserire un campo TOC e filtrare quali campi TC diventano voci.

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
java.lang.String - Un intervallo di livelli delle voci dell'indice da includere.
### getEntrySeparator() {#getEntrySeparator}
```
public String getEntrySeparator()
```


Ottiene una sequenza di caratteri che separa una voce dal suo numero di pagina.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
java.lang.String - Una sequenza di caratteri che separa una voce dal suo numero di pagina.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). Sia il codice del campo sia il risultato del campo dei campi figli sono inclusi.

 **Examples:** 

Mostra come inserire un campo in un documento usando un codice di campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Mostra come ottenere il codice di campo di un campo.

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


Restituisce il testo compreso tra l'inizio del campo e il separatore del campo (o la fine del campo se non c'è separatore).

 **Examples:** 

Mostra come ottenere il codice di campo di un campo.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true se i codici dei campi figli devono essere inclusi. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Ottiene un oggetto [FieldFormat](../../com.aspose.words/fieldformat/) che fornisce accesso tipizzato alla formattazione del campo.

 **Examples:** 

Mostra come formattare i risultati del campo.

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


Ottiene un intervallo di livelli di intestazione da includere.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
java.lang.String - Un intervallo di livelli di intestazione da includere.
### getHideInWebLayout() {#getHideInWebLayout}
```
public boolean getHideInWebLayout()
```


Ottiene se nascondere il leader di tabulazione e i numeri di pagina nella visualizzazione layout Web.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
boolean - Indica se nascondere il leader di tabulazione e i numeri di pagina nella visualizzazione layout Web.
### getInsertHyperlinks() {#getInsertHyperlinks}
```
public boolean getInsertHyperlinks()
```


Ottiene se rendere le voci del sommario dei collegamenti ipertestuali.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
boolean - Indica se rendere le voci dell'indice dei collegamenti ipertestuali.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Ottiene il LCID del campo.

 **Examples:** 

Mostra come inserire un campo e lavorare con la sua locale.

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
int - Il LCID del campo.
### getPageNumberOmittingLevelRange() {#getPageNumberOmittingLevelRange}
```
public String getPageNumberOmittingLevelRange()
```


Ottiene un intervallo di livelli delle voci del sommario da cui omettere i numeri di pagina.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
java.lang.String - Un intervallo di livelli delle voci dell'indice da cui omettere i numeri di pagina.
### getPrefixedSequenceIdentifier() {#getPrefixedSequenceIdentifier}
```
public String getPrefixedSequenceIdentifier()
```


Ottiene l'identificatore di una sequenza per la quale deve essere aggiunto un prefisso al numero di pagina della voce.

 **Examples:** 

Mostra come popolare un campo TOC con voci usando i campi SEQ.

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
java.lang.String - L'identificatore di una sequenza per la quale dovrebbe essere aggiunto un prefisso al numero di pagina della voce.
### getPreserveLineBreaks() {#getPreserveLineBreaks}
```
public boolean getPreserveLineBreaks()
```


Ottiene se preservare i caratteri di nuova riga all'interno delle voci della tabella.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
boolean - Indica se conservare i caratteri di nuova riga all'interno delle voci della tabella.
### getPreserveTabs() {#getPreserveTabs}
```
public boolean getPreserveTabs()
```


Ottiene se preservare le voci di tabulazione all'interno delle voci della tabella.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
boolean - Indica se conservare le voci di tabulazione all'interno delle voci della tabella.
### getResult() {#getResult}
```
public String getResult()
```


Ottiene il testo compreso tra il separatore del campo e la fine del campo.

 **Examples:** 

Mostra come inserire un campo in un documento usando un codice di campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Testo che si trova tra il separatore di campo e la fine del campo.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Ottiene il nodo che rappresenta il separatore di campo. Può essere `null`.

 **Examples:** 

Mostra come lavorare con una raccolta di campi.

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


Ottiene la sequenza di caratteri utilizzata per separare i numeri di sequenza dai numeri di pagina.

 **Examples:** 

Mostra come popolare un campo TOC con voci usando i campi SEQ.

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
java.lang.String - La sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Ottiene il nodo che rappresenta l'inizio del campo.

 **Examples:** 

Mostra come lavorare con una raccolta di campi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getTableOfFiguresLabel() {#getTableOfFiguresLabel}
```
public String getTableOfFiguresLabel()
```


Ottiene il nome dell'identificatore di sequenza utilizzato durante la creazione di un indice delle figure.

 **Examples:** 

Mostra come popolare un campo TOC con voci usando i campi SEQ.

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
java.lang.String - Il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella delle figure.
### getType() {#getType}
```
public int getType()
```


Ottiene il tipo di campo di Microsoft Word.

 **Examples:** 

Mostra come inserire un campo in un documento usando un codice di campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - Il tipo di campo di Microsoft Word. Il valore restituito è una delle costanti [FieldType](../../com.aspose.words/fieldtype/).
### getUseParagraphOutlineLevel() {#getUseParagraphOutlineLevel}
```
public boolean getUseParagraphOutlineLevel()
```


Ottiene se utilizzare il livello di contorno del paragrafo applicato.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
boolean - Indica se utilizzare il livello di contorno del paragrafo applicato.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Ottiene se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento.

 **Examples:** 

Mostra come utilizzare la proprietà speciale per aggiornare il risultato del campo.

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
boolean - Indica se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento.

 **Examples:** 

Mostra come utilizzare la proprietà speciale per aggiornare il risultato del campo.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Ottiene se il campo è bloccato (non deve ricalcolare il suo risultato).

 **Examples:** 

Mostra come lavorare con un nodo FieldStart.

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
boolean - Indica se il campo è bloccato (non dovrebbe ricalcolare il suo risultato).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Imposta se il campo è bloccato (non deve ricalcolare il suo risultato).

 **Examples:** 

Mostra come lavorare con un nodo FieldStart.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |

### remove() {#remove}
```
public Node remove()
```


Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce `null`.

 **Examples:** 

Mostra come rimuovere i campi da una raccolta di campi.

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

Mostra come elaborare i campi PRIVATE.

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


Imposta il nome del segnalibro che indica la parte del documento utilizzata per costruire la tabella.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome del segnalibro che indica la parte del documento usata per costruire la tabella. |

### setCaptionlessTableOfFiguresLabel(String value) {#setCaptionlessTableOfFiguresLabel-java.lang.String}
```
public void setCaptionlessTableOfFiguresLabel(String value)
```


Imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di un indice delle figure che non include l'etichetta e il numero della didascalia.

 **Examples:** 

Mostra come impostare il nome dell'identificatore di sequenza.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldToc fieldToc = (FieldToc)builder.insertField(FieldType.FIELD_TOC, true);
 fieldToc.setCaptionlessTableOfFiguresLabel("Test");

 Assert.assertEquals(" TOC  \\a Test", fieldToc.getFieldCode());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella delle figure che non include l'etichetta e il numero della didascalia. |

### setCustomStyles(String value) {#setCustomStyles-java.lang.String}
```
public void setCustomStyles(String value)
```


Imposta un elenco di stili diversi dagli stili di intestazione predefiniti da includere nel sommario.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Un elenco di stili diversi dagli stili di intestazione predefiniti da includere nell'indice. |

### setEntryIdentifier(String value) {#setEntryIdentifier-java.lang.String}
```
public void setEntryIdentifier(String value)
```


Imposta una stringa che deve corrispondere agli identificatori di tipo dei campi TC inclusi.

 **Examples:** 

Mostra come inserire un campo TOC e filtrare quali campi TC diventano voci.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Una stringa che dovrebbe corrispondere agli identificatori di tipo dei campi TC da includere. |

### setEntryLevelRange(String value) {#setEntryLevelRange-java.lang.String}
```
public void setEntryLevelRange(String value)
```


Imposta un intervallo di livelli delle voci del sommario da includere.

 **Examples:** 

Mostra come inserire un campo TOC e filtrare quali campi TC diventano voci.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Un intervallo di livelli delle voci dell'indice da includere. |

### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String}
```
public void setEntrySeparator(String value)
```


Imposta una sequenza di caratteri che separa una voce dal suo numero di pagina.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Una sequenza di caratteri che separa una voce dal suo numero di pagina. |

### setHeadingLevelRange(String value) {#setHeadingLevelRange-java.lang.String}
```
public void setHeadingLevelRange(String value)
```


Imposta un intervallo di livelli di intestazione da includere.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Un intervallo di livelli di intestazione da includere. |

### setHideInWebLayout(boolean value) {#setHideInWebLayout-boolean}
```
public void setHideInWebLayout(boolean value)
```


Imposta se nascondere il leader di tabulazione e i numeri di pagina nella visualizzazione layout Web.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se nascondere il leader di tabulazione e i numeri di pagina nella visualizzazione layout Web. |

### setInsertHyperlinks(boolean value) {#setInsertHyperlinks-boolean}
```
public void setInsertHyperlinks(boolean value)
```


Imposta se rendere le voci del sommario dei collegamenti ipertestuali.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se rendere i collegamenti ipertestuali le voci dell'indice. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Imposta il LCID del campo.

 **Examples:** 

Mostra come inserire un campo e lavorare con la sua locale.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il LCID del campo. |

### setPageNumberOmittingLevelRange(String value) {#setPageNumberOmittingLevelRange-java.lang.String}
```
public void setPageNumberOmittingLevelRange(String value)
```


Imposta un intervallo di livelli delle voci del sommario da cui omettere i numeri di pagina.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Un intervallo di livelli delle voci dell'indice da cui omettere i numeri di pagina. |

### setPrefixedSequenceIdentifier(String value) {#setPrefixedSequenceIdentifier-java.lang.String}
```
public void setPrefixedSequenceIdentifier(String value)
```


Imposta l'identificatore di una sequenza per la quale deve essere aggiunto un prefisso al numero di pagina della voce.

 **Examples:** 

Mostra come popolare un campo TOC con voci usando i campi SEQ.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | L'identificatore di una sequenza per la quale deve essere aggiunto un prefisso al numero di pagina della voce. |

### setPreserveLineBreaks(boolean value) {#setPreserveLineBreaks-boolean}
```
public void setPreserveLineBreaks(boolean value)
```


Imposta se preservare i caratteri di nuova riga all'interno delle voci della tabella.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se conservare i caratteri di nuova riga all'interno delle voci della tabella. |

### setPreserveTabs(boolean value) {#setPreserveTabs-boolean}
```
public void setPreserveTabs(boolean value)
```


Imposta se preservare le voci di tabulazione all'interno delle voci della tabella.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se conservare le tabulazioni all'interno delle voci della tabella. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Imposta il testo che si trova tra il separatore di campo e la fine del campo.

 **Examples:** 

Mostra come inserire un campo in un documento usando un codice di campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Testo che si trova tra il separatore di campo e la fine del campo. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String}
```
public void setSequenceSeparator(String value)
```


Imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza dai numeri di pagina.

 **Examples:** 

Mostra come popolare un campo TOC con voci usando i campi SEQ.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | La sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |

### setTableOfFiguresLabel(String value) {#setTableOfFiguresLabel-java.lang.String}
```
public void setTableOfFiguresLabel(String value)
```


Imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella delle figure.

 **Examples:** 

Mostra come popolare un campo TOC con voci usando i campi SEQ.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome dell'identificatore di sequenza utilizzato durante la creazione di un indice delle figure. |

### setUseParagraphOutlineLevel(boolean value) {#setUseParagraphOutlineLevel-boolean}
```
public void setUseParagraphOutlineLevel(boolean value)
```


Imposta se utilizzare il livello di contorno del paragrafo applicato.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se utilizzare il livello di contorno del paragrafo applicato. |

### unlink() {#unlink}
```
public boolean unlink()
```


Esegue lo scollegamento del campo.

 **Remarks:** 

Sostituisce il campo con il suo risultato più recente.

Alcuni campi, come i campi XE (Voce di indice) e SEQ (Sequenza), non possono essere scollegati.

 **Examples:** 

Mostra come scollegare un campo.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean - `true` se il campo è stato scollegato, altrimenti `false`.
### update() {#update}
```
public void update()
```


Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento.

 **Examples:** 

Mostra come inserire un campo in un documento utilizzando FieldType.

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

Mostra come formattare i risultati del campo.

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


Esegue un aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento.

 **Examples:** 

Mostra come preservare o scartare i campi INCLUDEPICTURE durante il caricamento di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| ignoreMergeFormat | boolean | Se `true` allora la formattazione diretta del risultato del campo viene abbandonata, indipendentemente dall'opzione MERGEFORMAT, altrimenti viene eseguito un aggiornamento normale. |

### updatePageNumbers() {#updatePageNumbers}
```
public boolean updatePageNumbers()
```


Aggiorna i numeri di pagina per gli elementi di questo indice.

 **Examples:** 

Mostra come inserire un indice e popolarlo con voci basate sugli stili di intestazione.

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
boolean - true se l'operazione ha avuto successo. Se uno dei segnalibri TOC correlati è stato rimosso, false verrà restituito.
