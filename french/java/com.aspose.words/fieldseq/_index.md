---
title: "FieldSeq"
linktitle: "FieldSeq"
second_title: "Aspose.Words pour Java"
description: "Implémente le champ SEQ en Java."
type: docs
weight: 284
url: /fr/java/com.aspose.words/fieldseq/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldSeq extends Field
```

Implémente le champ SEQ.

Pour en savoir plus, consultez l'article de documentation [ Working with Fields ][Working with Fields].

 **Remarks:** 

Numérote séquentiellement les chapitres, tableaux, figures et autres listes d'éléments définies par l'utilisateur dans un document.

 **Examples:** 

Montre comment remplir un champ de table des matières avec des entrées en utilisant des champs SEQ.

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

Montre comment créer une numérotation en utilisant des champs SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

Montre comment combiner la table des matières et les champs de séquence.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that contains the SEQ field,
 // and the number of the page that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // Configure this TOC field to have a SequenceIdentifier property with a value of "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // Configure this TOC field to only pick up SEQ fields that are within the bounds of a bookmark
 // named "TOCBookmark".
 fieldToc.setBookmarkName("TOCBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);

 Assert.assertEquals(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that has a sequence identifier that matches the TOC's
 // TableOfFiguresLabel property. This field will not create an entry in the TOC since it is outside
 // the bookmark's bounds designated by "BookmarkName".
 builder.write("MySequence #");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will not show up in the TOC because it is outside of the bookmark.");

 builder.startBookmark("TOCBookmark");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bookmark's bounds.
 // The paragraph that contains this field will show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will show up in the TOC next to the entry for the above caption.");

 // This SEQ field's sequence does not match the TOC's "TableOfFiguresLabel" property,
 // and is within the bounds of the bookmark. Its paragraph will not show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("OtherSequence");
 builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bounds of the bookmark.
 // This field also references another bookmark. The contents of that bookmark will appear in the TOC entry for this SEQ field.
 // The SEQ field itself will not display the contents of that bookmark.
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setBookmarkName("SEQBookmark");
 Assert.assertEquals(" SEQ  MySequence SEQBookmark", fieldSeq.getFieldCode());

 // Create a bookmark with contents that will show up in the TOC entry due to the above SEQ field referencing it.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("SEQBookmark");
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", text from inside SEQBookmark.");
 builder.endBookmark("SEQBookmark");

 builder.endBookmark("TOCBookmark");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.Bookmark.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getBookmarkName()](#getBookmarkName) | Obtient un nom de signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel. |
| [getDisplayResult()](#getDisplayResult) | Obtient le texte qui représente le résultat du champ affiché. |
| [getEnd()](#getEnd) | Obtient le nœud qui représente la fin du champ. |
| [getFieldCode()](#getFieldCode) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [getFormat()](#getFormat) | Obtient un objet [FieldFormat](../../com.aspose.words/fieldformat/) qui fournit un accès typé au formatage du champ. |
| [getInsertNextNumber()](#getInsertNextNumber) | Obtient si le prochain numéro de séquence doit être inséré pour l'élément spécifié. |
| [getLocaleId()](#getLocaleId) | Obtient le LCID du champ. |
| [getResetHeadingLevel()](#getResetHeadingLevel) | Obtient un nombre entier représentant le niveau de titre auquel réinitialiser le numéro de séquence. |
| [getResetNumber()](#getResetNumber) | Obtient un nombre entier auquel réinitialiser le numéro de séquence. |
| [getResult()](#getResult) | Obtient le texte qui se trouve entre le séparateur du champ et la fin du champ. |
| [getSeparator()](#getSeparator) | Obtient le nœud qui représente le séparateur de champ. |
| [getSequenceIdentifier()](#getSequenceIdentifier) | Obtient le nom attribué à la série d'éléments qui doivent être numérotés. |
| [getStart()](#getStart) | Obtient le nœud qui représente le début du champ. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Obtient le type de champ Microsoft Word. |
| [isDirty()](#isDirty) | Obtient si le résultat actuel du champ n’est plus correct (obsolète) en raison d’autres modifications apportées au document. |
| [isDirty(boolean value)](#isDirty-boolean) | Définit si le résultat actuel du champ n’est plus correct (obsolète) en raison d’autres modifications apportées au document. |
| [isLocked()](#isLocked) | Obtient si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [isLocked(boolean value)](#isLocked-boolean) | Définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [remove()](#remove) | Supprime le champ du document. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | Définit un nom de signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel. |
| [setInsertNextNumber(boolean value)](#setInsertNextNumber-boolean) | Définit si le prochain numéro de séquence doit être inséré pour l'élément spécifié. |
| [setLocaleId(int value)](#setLocaleId-int) | Définit le LCID du champ. |
| [setResetHeadingLevel(String value)](#setResetHeadingLevel-java.lang.String) | Définit un nombre entier représentant le niveau de titre auquel réinitialiser le numéro de séquence. |
| [setResetNumber(String value)](#setResetNumber-java.lang.String) | Définit un nombre entier auquel réinitialiser le numéro de séquence. |
| [setResult(String value)](#setResult-java.lang.String) | Définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [setSequenceIdentifier(String value)](#setSequenceIdentifier-java.lang.String) | Définit le nom attribué à la série d'éléments qui doivent être numérotés. |
| [unlink()](#unlink) | Effectue le détachement du champ. |
| [update()](#update) | Effectue la mise à jour du champ. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Effectue une mise à jour du champ. |
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


Obtient un nom de signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel.

 **Examples:** 

Montre comment combiner la table des matières et les champs de séquence.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that contains the SEQ field,
 // and the number of the page that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // Configure this TOC field to have a SequenceIdentifier property with a value of "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // Configure this TOC field to only pick up SEQ fields that are within the bounds of a bookmark
 // named "TOCBookmark".
 fieldToc.setBookmarkName("TOCBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);

 Assert.assertEquals(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that has a sequence identifier that matches the TOC's
 // TableOfFiguresLabel property. This field will not create an entry in the TOC since it is outside
 // the bookmark's bounds designated by "BookmarkName".
 builder.write("MySequence #");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will not show up in the TOC because it is outside of the bookmark.");

 builder.startBookmark("TOCBookmark");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bookmark's bounds.
 // The paragraph that contains this field will show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will show up in the TOC next to the entry for the above caption.");

 // This SEQ field's sequence does not match the TOC's "TableOfFiguresLabel" property,
 // and is within the bounds of the bookmark. Its paragraph will not show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("OtherSequence");
 builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bounds of the bookmark.
 // This field also references another bookmark. The contents of that bookmark will appear in the TOC entry for this SEQ field.
 // The SEQ field itself will not display the contents of that bookmark.
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setBookmarkName("SEQBookmark");
 Assert.assertEquals(" SEQ  MySequence SEQBookmark", fieldSeq.getFieldCode());

 // Create a bookmark with contents that will show up in the TOC entry due to the above SEQ field referencing it.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("SEQBookmark");
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", text from inside SEQBookmark.");
 builder.endBookmark("SEQBookmark");

 builder.endBookmark("TOCBookmark");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.Bookmark.docx");
 
```

**Returns:**
java.lang.String - Un nom de signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Obtient le texte qui représente le résultat du champ affiché.

 **Remarks:** 

La méthode [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) doit être appelée pour obtenir la valeur correcte des champs [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) et [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/).

 **Examples:** 

Montre comment obtenir le texte réel affiché par un champ dans le document.

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
java.lang.String - Le texte qui représente le résultat affiché du champ.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Obtient le nœud qui représente la fin du champ.

 **Examples:** 

Montre comment travailler avec une collection de champs.

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
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s’il n’y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus.

 **Examples:** 

Montre comment insérer un champ dans un document en utilisant un code de champ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Montre comment obtenir le code de champ d’un champ.

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


Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur).

 **Examples:** 

Montre comment obtenir le code de champ d’un champ.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true si les codes de champ enfants doivent être inclus. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Obtient un objet [FieldFormat](../../com.aspose.words/fieldformat/) qui fournit un accès typé au formatage du champ.

 **Examples:** 

Montre comment formater les résultats de champ.

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
### getInsertNextNumber() {#getInsertNextNumber}
```
public boolean getInsertNextNumber()
```


Obtient si le prochain numéro de séquence doit être inséré pour l'élément spécifié.

 **Examples:** 

Montre comment créer une numérotation en utilisant des champs SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Returns:**
boolean - Indique si le prochain numéro de séquence doit être inséré pour l'élément spécifié.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Obtient le LCID du champ.

 **Examples:** 

Montre comment insérer un champ et travailler avec sa locale.

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
int - Le LCID du champ.
### getResetHeadingLevel() {#getResetHeadingLevel}
```
public String getResetHeadingLevel()
```


Obtient un nombre entier représentant le niveau de titre auquel réinitialiser le numéro de séquence. Retourne -1 si le nombre est absent.

 **Examples:** 

Montre comment créer une numérotation en utilisant des champs SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Returns:**
java.lang.String - Un nombre entier représentant le niveau de titre auquel réinitialiser le numéro de séquence.
### getResetNumber() {#getResetNumber}
```
public String getResetNumber()
```


Obtient un nombre entier auquel réinitialiser le numéro de séquence. Retourne -1 si le nombre est absent.

 **Examples:** 

Montre comment créer une numérotation en utilisant des champs SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Returns:**
java.lang.String - Un nombre entier auquel réinitialiser le numéro de séquence.
### getResult() {#getResult}
```
public String getResult()
```


Obtient le texte qui se trouve entre le séparateur du champ et la fin du champ.

 **Examples:** 

Montre comment insérer un champ dans un document en utilisant un code de champ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Texte qui se trouve entre le séparateur de champ et la fin du champ.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Obtient le nœud qui représente le séparateur de champ. Peut être  null .

 **Examples:** 

Montre comment travailler avec une collection de champs.

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
### getSequenceIdentifier() {#getSequenceIdentifier}
```
public String getSequenceIdentifier()
```


Obtient le nom attribué à la série d'éléments qui doivent être numérotés.

 **Examples:** 

Montre comment remplir un champ de table des matières avec des entrées en utilisant des champs SEQ.

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

Montre comment créer une numérotation en utilisant des champs SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Returns:**
java.lang.String - Le nom attribué à la série d'éléments qui doivent être numérotés.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Obtient le nœud qui représente le début du champ.

 **Examples:** 

Montre comment travailler avec une collection de champs.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getType() {#getType}
```
public int getType()
```


Obtient le type de champ Microsoft Word.

 **Examples:** 

Montre comment insérer un champ dans un document en utilisant un code de champ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - Le type de champ Microsoft Word. La valeur retournée est l'une des constantes [FieldType](../../com.aspose.words/fieldtype/).
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Obtient si le résultat actuel du champ n’est plus correct (obsolète) en raison d’autres modifications apportées au document.

 **Examples:** 

Montre comment utiliser la propriété spéciale pour mettre à jour le résultat du champ.

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
boolean - Indique si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Définit si le résultat actuel du champ n’est plus correct (obsolète) en raison d’autres modifications apportées au document.

 **Examples:** 

Montre comment utiliser la propriété spéciale pour mettre à jour le résultat du champ.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Indique si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Obtient si le champ est verrouillé (ne doit pas recalculer son résultat).

 **Examples:** 

Montre comment travailler avec un nœud FieldStart.

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
boolean - Indique si le champ est verrouillé (ne doit pas recalculer son résultat).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Définit si le champ est verrouillé (ne doit pas recalculer son résultat).

 **Examples:** 

Montre comment travailler avec un nœud FieldStart.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Indique si le champ est verrouillé (ne doit pas recalculer son résultat). |

### remove() {#remove}
```
public Node remove()
```


Supprime le champ du document. Retourne un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, retourne le paragraphe parent. Si le champ est déjà supprimé, retourne  null .

 **Examples:** 

Montre comment supprimer des champs d'une collection de champs.

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

Montre comment traiter les champs PRIVATE.

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


Définit un nom de signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel.

 **Examples:** 

Montre comment combiner la table des matières et les champs de séquence.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that contains the SEQ field,
 // and the number of the page that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // Configure this TOC field to have a SequenceIdentifier property with a value of "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // Configure this TOC field to only pick up SEQ fields that are within the bounds of a bookmark
 // named "TOCBookmark".
 fieldToc.setBookmarkName("TOCBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);

 Assert.assertEquals(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that has a sequence identifier that matches the TOC's
 // TableOfFiguresLabel property. This field will not create an entry in the TOC since it is outside
 // the bookmark's bounds designated by "BookmarkName".
 builder.write("MySequence #");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will not show up in the TOC because it is outside of the bookmark.");

 builder.startBookmark("TOCBookmark");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bookmark's bounds.
 // The paragraph that contains this field will show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will show up in the TOC next to the entry for the above caption.");

 // This SEQ field's sequence does not match the TOC's "TableOfFiguresLabel" property,
 // and is within the bounds of the bookmark. Its paragraph will not show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("OtherSequence");
 builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bounds of the bookmark.
 // This field also references another bookmark. The contents of that bookmark will appear in the TOC entry for this SEQ field.
 // The SEQ field itself will not display the contents of that bookmark.
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setBookmarkName("SEQBookmark");
 Assert.assertEquals(" SEQ  MySequence SEQBookmark", fieldSeq.getFieldCode());

 // Create a bookmark with contents that will show up in the TOC entry due to the above SEQ field referencing it.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("SEQBookmark");
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", text from inside SEQBookmark.");
 builder.endBookmark("SEQBookmark");

 builder.endBookmark("TOCBookmark");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.Bookmark.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Un nom de signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel. |

### setInsertNextNumber(boolean value) {#setInsertNextNumber-boolean}
```
public void setInsertNextNumber(boolean value)
```


Définit si le prochain numéro de séquence doit être inséré pour l'élément spécifié.

 **Examples:** 

Montre comment créer une numérotation en utilisant des champs SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Indique si le prochain numéro de séquence doit être inséré pour l'élément spécifié. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Définit le LCID du champ.

 **Examples:** 

Montre comment insérer un champ et travailler avec sa locale.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le LCID du champ. |

### setResetHeadingLevel(String value) {#setResetHeadingLevel-java.lang.String}
```
public void setResetHeadingLevel(String value)
```


Définit un nombre entier représentant le niveau de titre auquel réinitialiser le numéro de séquence. Retourne -1 si le nombre est absent.

 **Examples:** 

Montre comment créer une numérotation en utilisant des champs SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Un nombre entier représentant le niveau de titre auquel réinitialiser le numéro de séquence. |

### setResetNumber(String value) {#setResetNumber-java.lang.String}
```
public void setResetNumber(String value)
```


Définit un nombre entier auquel réinitialiser le numéro de séquence. Retourne -1 si le nombre est absent.

 **Examples:** 

Montre comment créer une numérotation en utilisant des champs SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Un nombre entier auquel réinitialiser le numéro de séquence. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Définit le texte qui se trouve entre le séparateur de champ et la fin du champ.

 **Examples:** 

Montre comment insérer un champ dans un document en utilisant un code de champ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Texte qui se trouve entre le séparateur de champ et la fin du champ. |

### setSequenceIdentifier(String value) {#setSequenceIdentifier-java.lang.String}
```
public void setSequenceIdentifier(String value)
```


Définit le nom attribué à la série d'éléments qui doivent être numérotés.

 **Examples:** 

Montre comment remplir un champ de table des matières avec des entrées en utilisant des champs SEQ.

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

Montre comment créer une numérotation en utilisant des champs SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom attribué à la série d'éléments qui doivent être numérotés. |

### unlink() {#unlink}
```
public boolean unlink()
```


Effectue le détachement du champ.

 **Remarks:** 

Remplace le champ par son résultat le plus récent.

Certains champs, tels que les champs XE (Entrée d'index) et SEQ (Séquence), ne peuvent pas être dissociés.

 **Examples:** 

Montre comment dissocier un champ.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  si le champ a été dissocié, sinon  false .
### update() {#update}
```
public void update()
```


Effectue la mise à jour du champ. Lève une exception si le champ est déjà en cours de mise à jour.

 **Examples:** 

Montre comment insérer un champ dans un document en utilisant FieldType.

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

Montre comment formater les résultats de champ.

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


Effectue une mise à jour du champ. Lève une exception si le champ est déjà en cours de mise à jour.

 **Examples:** 

Montre comment conserver ou ignorer les champs INCLUDEPICTURE lors du chargement d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | boolean | Si  true  alors le formatage direct du résultat du champ est abandonné, quel que soit le commutateur MERGEFORMAT, sinon une mise à jour normale est effectuée. |

