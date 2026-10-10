---
title: "EndnoteOptions"
linktitle: "EndnoteOptions"
second_title: "Aspose.Words pour Java"
description: "Représente les options de numérotation des notes de fin pour un document ou une section en Java."
type: docs
weight: 189
url: /fr/java/com.aspose.words/endnoteoptions/
---

**Inheritance:**
java.lang.Object
```
public class EndnoteOptions
```

Représente les options de numérotation des notes de fin pour un document ou une section.

Pour en savoir plus, consultez l'article de documentation [ Working with Footnote and Endnote ][Working with Footnote and Endnote].

 **Examples:** 

Montre comment sélectionner un emplacement différent où le document collecte et affiche ses notes de fin.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // An endnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting an endnote adds a small superscript reference symbol
 // at the main body text where we insert the endnote.
 // Each endnote also creates an entry at the end of the document, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote contents.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("This is the second section.");

 // We can use the "Position" property to determine where the document will place all its endnotes.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
 // every footnote will show up in a collection at the end of the document. This is the default value.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
 // every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
 doc.getEndnoteOptions().setPosition(endnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionEndnote.docx");
 
```

Montre comment changer le style de numérotation des marques de référence des notes de bas de page/notes de fin.

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

Montre comment redémarrer la numérotation des notes de bas de page/notes de fin à certains endroits du document.

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

Montre comment définir le numéro à partir duquel le document commence le comptage des notes de bas de page/notes de fin.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getLocation()](#getLocation) |  |
| [getNumberStyle()](#getNumberStyle) | Spécifie le format de nombre pour les notes de fin numérotées automatiquement. |
| [getPosition()](#getPosition) | Spécifie la position des notes de fin. |
| [getRestartRule()](#getRestartRule) | Détermine quand la numérotation automatique redémarre. |
| [getStartNumber()](#getStartNumber) | Spécifie le numéro ou le caractère de départ pour la première note de fin numérotée automatiquement. |
| [setLocation(int value)](#setLocation-int) |  |
| [setNumberStyle(int value)](#setNumberStyle-int) | Spécifie le format de nombre pour les notes de fin numérotées automatiquement. |
| [setPosition(int value)](#setPosition-int) | Spécifie la position des notes de fin. |
| [setRestartRule(int value)](#setRestartRule-int) | Détermine quand la numérotation automatique redémarre. |
| [setStartNumber(int value)](#setStartNumber-int) | Spécifie le numéro ou le caractère de départ pour la première note de fin numérotée automatiquement. |
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


Spécifie le format de nombre pour les notes de fin numérotées automatiquement.

 **Remarks:** 

Tous les styles de numérotation ne sont pas applicables à cette propriété. Pour la liste des styles de numérotation applicables, consultez la boîte de dialogue Insérer une note de bas de page ou une note de fin dans Microsoft Word. Si vous choisissez un style de numérotation qui n'est pas applicable, Microsoft Word reviendra à la valeur par défaut.

 **Examples:** 

Montre comment changer le style de numérotation des marques de référence des notes de bas de page/notes de fin.

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
int - La valeur int correspondante. La valeur retournée est l'une des constantes [NumberStyle](../../com.aspose.words/numberstyle/).
### getPosition() {#getPosition}
```
public int getPosition()
```


Spécifie la position des notes de fin.

 **Examples:** 

Montre comment sélectionner un emplacement différent où le document collecte et affiche ses notes de fin.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // An endnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting an endnote adds a small superscript reference symbol
 // at the main body text where we insert the endnote.
 // Each endnote also creates an entry at the end of the document, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote contents.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("This is the second section.");

 // We can use the "Position" property to determine where the document will place all its endnotes.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
 // every footnote will show up in a collection at the end of the document. This is the default value.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
 // every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
 doc.getEndnoteOptions().setPosition(endnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionEndnote.docx");
 
```

**Returns:**
int - La valeur int correspondante. La valeur retournée est l'une des constantes [EndnotePosition](../../com.aspose.words/endnoteposition/) .
### getRestartRule() {#getRestartRule}
```
public int getRestartRule()
```


Détermine quand la numérotation automatique redémarre.

 **Remarks:** 

Toutes les valeurs ne s'appliquent pas aux notes de fin. Pour déterminer quelles valeurs sont applicables, voir [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/).

 **Examples:** 

Montre comment redémarrer la numérotation des notes de bas de page/notes de fin à certains endroits du document.

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
int - La valeur int correspondante. La valeur retournée est l'une des constantes [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/).
### getStartNumber() {#getStartNumber}
```
public int getStartNumber()
```


Spécifie le numéro ou le caractère de départ pour la première note de fin numérotée automatiquement.

 **Remarks:** 

Cette propriété n'a d'effet que lorsque [getRestartRule()](../../com.aspose.words/endnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions/\#setRestartRule-int) est définie sur [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

 **Examples:** 

Montre comment définir le numéro à partir duquel le document commence le comptage des notes de bas de page/notes de fin.

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
int - La valeur int correspondante.
### setLocation(int value) {#setLocation-int}
```
public void setLocation(int value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int |  |

### setNumberStyle(int value) {#setNumberStyle-int}
```
public void setNumberStyle(int value)
```


Spécifie le format de nombre pour les notes de fin numérotées automatiquement.

 **Remarks:** 

Tous les styles de numérotation ne sont pas applicables à cette propriété. Pour la liste des styles de numérotation applicables, consultez la boîte de dialogue Insérer une note de bas de page ou une note de fin dans Microsoft Word. Si vous choisissez un style de numérotation qui n'est pas applicable, Microsoft Word reviendra à la valeur par défaut.

 **Examples:** 

Montre comment changer le style de numérotation des marques de référence des notes de bas de page/notes de fin.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [NumberStyle](../../com.aspose.words/numberstyle/). |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Spécifie la position des notes de fin.

 **Examples:** 

Montre comment sélectionner un emplacement différent où le document collecte et affiche ses notes de fin.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // An endnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting an endnote adds a small superscript reference symbol
 // at the main body text where we insert the endnote.
 // Each endnote also creates an entry at the end of the document, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote contents.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("This is the second section.");

 // We can use the "Position" property to determine where the document will place all its endnotes.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
 // every footnote will show up in a collection at the end of the document. This is the default value.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
 // every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
 doc.getEndnoteOptions().setPosition(endnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionEndnote.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [EndnotePosition](../../com.aspose.words/endnoteposition/) . |

### setRestartRule(int value) {#setRestartRule-int}
```
public void setRestartRule(int value)
```


Détermine quand la numérotation automatique redémarre.

 **Remarks:** 

Toutes les valeurs ne s'appliquent pas aux notes de fin. Pour déterminer quelles valeurs sont applicables, voir [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/).

 **Examples:** 

Montre comment redémarrer la numérotation des notes de bas de page/notes de fin à certains endroits du document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/). |

### setStartNumber(int value) {#setStartNumber-int}
```
public void setStartNumber(int value)
```


Spécifie le numéro ou le caractère de départ pour la première note de fin numérotée automatiquement.

 **Remarks:** 

Cette propriété n'a d'effet que lorsque [getRestartRule()](../../com.aspose.words/endnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions/\#setRestartRule-int) est définie sur [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

 **Examples:** 

Montre comment définir le numéro à partir duquel le document commence le comptage des notes de bas de page/notes de fin.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

