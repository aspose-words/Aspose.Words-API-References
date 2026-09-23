---
title: "FootnoteOptions"
linktitle: "FootnoteOptions"
second_title: "Aspose.Words per Java"
description: "Rappresenta le opzioni di numerazione delle note a piè di pagina per un documento o una sezione in Java."
type: docs
weight: 341
url: /it/java/com.aspose.words/footnoteoptions/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteOptions
```

Rappresenta le opzioni di numerazione delle note a piè di pagina per un documento o una sezione.

Per saperne di più, visita l'articolo di documentazione [ Working with Footnote and Endnote ][Working with Footnote and Endnote] .

 **Examples:** 

Mostra come suddividere la sezione delle note a piè di pagina in un determinato numero di colonne.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");
 doc.getFootnoteOptions().setColumns(2);
 doc.save(getArtifactsDir() + "Document.FootnoteColumns.docx");
 
```

Mostra come selezionare un luogo diverso in cui il documento raccoglie e visualizza le sue note a piè di pagina.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A footnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote.
 // Each footnote also creates an entry at the bottom of the page, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertFootnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote contents.");

 // We can use the "Position" property to determine where the document will place all its footnotes.
 // If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
 // every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
 // If we set the value of the "Position" property to "FootnotePosition.BeneathText",
 // every footnote will show up at the end of the page's text that contains its reference mark.
 doc.getFootnoteOptions().setPosition(footnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionFootnote.docx");
 
```

Mostra come cambiare lo stile numerico dei segni di riferimento di note a piè di pagina/fine.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.", "Custom footnote reference mark");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.", "Custom endnote reference mark");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
 // and endnotes display their numbers in lowercase Roman numerals.
 Assert.assertEquals(NumberStyle.ARABIC, doc.getFootnoteOptions().getNumberStyle());
 Assert.assertEquals(NumberStyle.LOWERCASE_ROMAN, doc.getEndnoteOptions().getNumberStyle());

 // We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
 // This will not affect footnotes/endnotes with custom reference marks.
 doc.getFootnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_LETTER);

 doc.save(getArtifactsDir() + "InlineStory.RefMarkNumberStyle.docx");
 
```

Mostra come riavviare la numerazione delle note a piè di pagina/fine in determinati punti del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 4.");

 builder.insertBreak(BreakType.PAGE_BREAK);

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 4.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and endnotes and does not restart these counts at any point.
 Assert.assertEquals(doc.getFootnoteOptions().getRestartRule(), FootnoteNumberingRule.DEFAULT);
 Assert.assertEquals(FootnoteNumberingRule.DEFAULT, FootnoteNumberingRule.CONTINUOUS);

 // We can use the "RestartRule" property to get the document to restart
 // the footnote/endnote counts at a new page or section.
 doc.getFootnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 doc.getEndnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_SECTION);

 doc.save(getArtifactsDir() + "InlineStory.NumberingRule.docx");
 
```

Mostra come impostare un numero a partire dal quale il documento inizia il conteggio delle note a piè di pagina/fine.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes, which both begin at 1.
 Assert.assertEquals(1, doc.getFootnoteOptions().getStartNumber());
 Assert.assertEquals(1, doc.getEndnoteOptions().getStartNumber());

 // We can use the "StartNumber" property to get the document to
 // begin a footnote or endnote count at a different number.
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.ARABIC);
 doc.getEndnoteOptions().setStartNumber(50);

 doc.save(getArtifactsDir() + "InlineStory.StartNumber.docx");
 
```


[Working with Footnote and Endnote]: https://docs.aspose.com/words/java/working-with-footnote-and-endnote/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getColumns()](#getColumns) | Specifica il numero di colonne con cui è formattata l'area delle note a piè di pagina. |
| [getLocation()](#getLocation) |  |
| [getNumberStyle()](#getNumberStyle) | Specifica il formato numerico per le note a piè di pagina numerate automaticamente. |
| [getPosition()](#getPosition) | Specifica la posizione delle note a piè di pagina. |
| [getRestartRule()](#getRestartRule) | Determina quando la numerazione automatica si riavvia. |
| [getStartNumber()](#getStartNumber) | Specifica il numero o il carattere iniziale per le prime note a piè di pagina numerate automaticamente. |
| [setColumns(int value)](#setColumns-int) | Specifica il numero di colonne con cui è formattata l'area delle note a piè di pagina. |
| [setLocation(int value)](#setLocation-int) |  |
| [setNumberStyle(int value)](#setNumberStyle-int) | Specifica il formato numerico per le note a piè di pagina numerate automaticamente. |
| [setPosition(int value)](#setPosition-int) | Specifica la posizione delle note a piè di pagina. |
| [setRestartRule(int value)](#setRestartRule-int) | Determina quando la numerazione automatica si riavvia. |
| [setStartNumber(int value)](#setStartNumber-int) | Specifica il numero o il carattere iniziale per le prime note a piè di pagina numerate automaticamente. |
### getColumns() {#getColumns}
```
public int getColumns()
```


Specifica il numero di colonne con cui è formattata l'area delle note a piè di pagina.

 **Remarks:** 

Se questa proprietà ha valore 0, l'area delle note a piè di pagina è formattata con un numero di colonne basato sul numero di colonne della pagina visualizzata. Il valore predefinito è 0.

 **Examples:** 

Mostra come suddividere la sezione delle note a piè di pagina in un determinato numero di colonne.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");
 doc.getFootnoteOptions().setColumns(2);
 doc.save(getArtifactsDir() + "Document.FootnoteColumns.docx");
 
```

**Returns:**
int - Il valore  int  corrispondente.
### getLocation() {#getLocation}
```
public int getLocation()
```




**Returns:**
int
### getNumberStyle() {#getNumberStyle}
```
public int getNumberStyle()
```


Specifica il formato numerico per le note a piè di pagina numerate automaticamente.

 **Remarks:** 

Non tutti gli stili numerici sono applicabili a questa proprietà. Per l'elenco degli stili numerici applicabili, vedere la finestra di dialogo Inserisci nota a piè di pagina o nota a fine in Microsoft Word. Se si seleziona uno stile numerico non applicabile, Microsoft Word tornerà a un valore predefinito.

 **Examples:** 

Mostra come cambiare lo stile numerico dei segni di riferimento di note a piè di pagina/fine.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.", "Custom footnote reference mark");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.", "Custom endnote reference mark");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
 // and endnotes display their numbers in lowercase Roman numerals.
 Assert.assertEquals(NumberStyle.ARABIC, doc.getFootnoteOptions().getNumberStyle());
 Assert.assertEquals(NumberStyle.LOWERCASE_ROMAN, doc.getEndnoteOptions().getNumberStyle());

 // We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
 // This will not affect footnotes/endnotes with custom reference marks.
 doc.getFootnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_LETTER);

 doc.save(getArtifactsDir() + "InlineStory.RefMarkNumberStyle.docx");
 
```

**Returns:**
int - Il valore intero corrispondente. Il valore restituito è una delle costanti [NumberStyle](../../com.aspose.words/numberstyle/) .
### getPosition() {#getPosition}
```
public int getPosition()
```


Specifica la posizione delle note a piè di pagina.

 **Examples:** 

Mostra come selezionare un luogo diverso in cui il documento raccoglie e visualizza le sue note a piè di pagina.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A footnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote.
 // Each footnote also creates an entry at the bottom of the page, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertFootnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote contents.");

 // We can use the "Position" property to determine where the document will place all its footnotes.
 // If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
 // every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
 // If we set the value of the "Position" property to "FootnotePosition.BeneathText",
 // every footnote will show up at the end of the page's text that contains its reference mark.
 doc.getFootnoteOptions().setPosition(footnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionFootnote.docx");
 
```

**Returns:**
int - Il valore intero corrispondente. Il valore restituito è una delle costanti [FootnotePosition](../../com.aspose.words/footnoteposition/) .
### getRestartRule() {#getRestartRule}
```
public int getRestartRule()
```


Determina quando la numerazione automatica si riavvia.

 **Examples:** 

Mostra come riavviare la numerazione delle note a piè di pagina/fine in determinati punti del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 4.");

 builder.insertBreak(BreakType.PAGE_BREAK);

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 4.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and endnotes and does not restart these counts at any point.
 Assert.assertEquals(doc.getFootnoteOptions().getRestartRule(), FootnoteNumberingRule.DEFAULT);
 Assert.assertEquals(FootnoteNumberingRule.DEFAULT, FootnoteNumberingRule.CONTINUOUS);

 // We can use the "RestartRule" property to get the document to restart
 // the footnote/endnote counts at a new page or section.
 doc.getFootnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 doc.getEndnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_SECTION);

 doc.save(getArtifactsDir() + "InlineStory.NumberingRule.docx");
 
```

**Returns:**
int - Il valore intero corrispondente. Il valore restituito è una delle costanti [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/) .
### getStartNumber() {#getStartNumber}
```
public int getStartNumber()
```


Specifica il numero o il carattere iniziale per le prime note a piè di pagina numerate automaticamente.

 **Remarks:** 

Questa proprietà ha effetto solo quando [getRestartRule()](../../com.aspose.words/footnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions/\#setRestartRule-int) è impostata su [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

 **Examples:** 

Mostra come impostare un numero a partire dal quale il documento inizia il conteggio delle note a piè di pagina/fine.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes, which both begin at 1.
 Assert.assertEquals(1, doc.getFootnoteOptions().getStartNumber());
 Assert.assertEquals(1, doc.getEndnoteOptions().getStartNumber());

 // We can use the "StartNumber" property to get the document to
 // begin a footnote or endnote count at a different number.
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.ARABIC);
 doc.getEndnoteOptions().setStartNumber(50);

 doc.save(getArtifactsDir() + "InlineStory.StartNumber.docx");
 
```

**Returns:**
int - Il valore  int  corrispondente.
### setColumns(int value) {#setColumns-int}
```
public void setColumns(int value)
```


Specifica il numero di colonne con cui è formattata l'area delle note a piè di pagina.

 **Remarks:** 

Se questa proprietà ha valore 0, l'area delle note a piè di pagina è formattata con un numero di colonne basato sul numero di colonne della pagina visualizzata. Il valore predefinito è 0.

 **Examples:** 

Mostra come suddividere la sezione delle note a piè di pagina in un determinato numero di colonne.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");
 doc.getFootnoteOptions().setColumns(2);
 doc.save(getArtifactsDir() + "Document.FootnoteColumns.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setLocation(int value) {#setLocation-int}
```
public void setLocation(int value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int |  |

### setNumberStyle(int value) {#setNumberStyle-int}
```
public void setNumberStyle(int value)
```


Specifica il formato numerico per le note a piè di pagina numerate automaticamente.

 **Remarks:** 

Non tutti gli stili numerici sono applicabili a questa proprietà. Per l'elenco degli stili numerici applicabili, vedere la finestra di dialogo Inserisci nota a piè di pagina o nota a fine in Microsoft Word. Se si seleziona uno stile numerico non applicabile, Microsoft Word tornerà a un valore predefinito.

 **Examples:** 

Mostra come cambiare lo stile numerico dei segni di riferimento di note a piè di pagina/fine.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.", "Custom footnote reference mark");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.", "Custom endnote reference mark");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
 // and endnotes display their numbers in lowercase Roman numerals.
 Assert.assertEquals(NumberStyle.ARABIC, doc.getFootnoteOptions().getNumberStyle());
 Assert.assertEquals(NumberStyle.LOWERCASE_ROMAN, doc.getEndnoteOptions().getNumberStyle());

 // We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
 // This will not affect footnotes/endnotes with custom reference marks.
 doc.getFootnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_LETTER);

 doc.save(getArtifactsDir() + "InlineStory.RefMarkNumberStyle.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere una delle costanti [NumberStyle](../../com.aspose.words/numberstyle/) . |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Specifica la posizione delle note a piè di pagina.

 **Examples:** 

Mostra come selezionare un luogo diverso in cui il documento raccoglie e visualizza le sue note a piè di pagina.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A footnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote.
 // Each footnote also creates an entry at the bottom of the page, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertFootnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote contents.");

 // We can use the "Position" property to determine where the document will place all its footnotes.
 // If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
 // every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
 // If we set the value of the "Position" property to "FootnotePosition.BeneathText",
 // every footnote will show up at the end of the page's text that contains its reference mark.
 doc.getFootnoteOptions().setPosition(footnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionFootnote.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere uno dei costanti di [FootnotePosition](../../com.aspose.words/footnoteposition/). |

### setRestartRule(int value) {#setRestartRule-int}
```
public void setRestartRule(int value)
```


Determina quando la numerazione automatica si riavvia.

 **Examples:** 

Mostra come riavviare la numerazione delle note a piè di pagina/fine in determinati punti del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 4.");

 builder.insertBreak(BreakType.PAGE_BREAK);

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 4.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and endnotes and does not restart these counts at any point.
 Assert.assertEquals(doc.getFootnoteOptions().getRestartRule(), FootnoteNumberingRule.DEFAULT);
 Assert.assertEquals(FootnoteNumberingRule.DEFAULT, FootnoteNumberingRule.CONTINUOUS);

 // We can use the "RestartRule" property to get the document to restart
 // the footnote/endnote counts at a new page or section.
 doc.getFootnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 doc.getEndnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_SECTION);

 doc.save(getArtifactsDir() + "InlineStory.NumberingRule.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere uno dei costanti di [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/). |

### setStartNumber(int value) {#setStartNumber-int}
```
public void setStartNumber(int value)
```


Specifica il numero o il carattere iniziale per le prime note a piè di pagina numerate automaticamente.

 **Remarks:** 

Questa proprietà ha effetto solo quando [getRestartRule()](../../com.aspose.words/footnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions/\#setRestartRule-int) è impostata su [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

 **Examples:** 

Mostra come impostare un numero a partire dal quale il documento inizia il conteggio delle note a piè di pagina/fine.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes, which both begin at 1.
 Assert.assertEquals(1, doc.getFootnoteOptions().getStartNumber());
 Assert.assertEquals(1, doc.getEndnoteOptions().getStartNumber());

 // We can use the "StartNumber" property to get the document to
 // begin a footnote or endnote count at a different number.
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.ARABIC);
 doc.getEndnoteOptions().setStartNumber(50);

 doc.save(getArtifactsDir() + "InlineStory.StartNumber.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

