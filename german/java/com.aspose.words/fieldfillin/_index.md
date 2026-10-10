---
title: "FieldFillIn"
linktitle: "FieldFillIn"
second_title: "Aspose.Words für Java"
description: "Implementiert das FILLIN‑Feld in Java."
type: docs
weight: 232
url: /de/java/com.aspose.words/fieldfillin/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldFillIn extends Field
```

Implementiert das FILLIN-Feld.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Fields ][Working with Fields].

 **Remarks:** 

Fordert den Benutzer auf, Text einzugeben.

 **Examples:** 

Zeigt, wie das FILLIN‑Feld verwendet wird, um den Benutzer zu einer Antwort aufzufordern.

```

 public void fieldFillIn() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a FILLIN field. When we manually update this field in Microsoft Word,
     // it will prompt us to enter a response. The field will then display the response as text.
     FieldFillIn field = (FieldFillIn) builder.insertField(FieldType.FIELD_FILL_IN, true);
     field.setPromptText("Please enter a response:");
     field.setDefaultResponse("A default response.");

     // We can also use these fields to ask the user for a unique response for each page
     // created during a mail merge done using Microsoft Word.
     field.setPromptOnceOnMailMerge(true);

     Assert.assertEquals(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.getFieldCode());

     FieldMergeField mergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     mergeField.setFieldName("MergeField");

     // If we perform a mail merge programmatically, we can use a custom prompt respondent
     // to automatically edit responses for FILLIN fields that the mail merge encounters.
     doc.getFieldOptions().setUserPromptRespondent(new PromptRespondent());
     doc.getMailMerge().execute(new String[]{"MergeField"}, new Object[]{""});

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.FILLIN.docx");
 }

 /// 
 /// Prepends a line to the default response of every FILLIN field during a mail merge.
 /// 
 private static class PromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response modified by PromptRespondent. " + defaultResponse;
     }
 }
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getDefaultResponse()](#getDefaultResponse) | Liest die Standardantwort des Benutzers (Anfangswert im Eingabefenster). |
| [getDisplayResult()](#getDisplayResult) | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [getEnd()](#getEnd) | Liefert den Knoten, der das Feldende darstellt. |
| [getFieldCode()](#getFieldCode) | Gibt den Text zwischen Feldanfang und Feldtrennzeichen zurück (oder das Feldende, wenn kein Trennzeichen vorhanden ist). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Gibt den Text zwischen Feldanfang und Feldtrennzeichen zurück (oder das Feldende, wenn kein Trennzeichen vorhanden ist). |
| [getFormat()](#getFormat) | Liefert ein [FieldFormat](../../com.aspose.words/fieldformat/)‑Objekt, das typisierten Zugriff auf die Formatierung des Feldes ermöglicht. |
| [getLocaleId()](#getLocaleId) | Liefert die LCID des Feldes. |
| [getPromptOnceOnMailMerge()](#getPromptOnceOnMailMerge) | Liest, ob die Benutzerantwort pro Seriendruckvorgang einmal empfangen werden soll. |
| [getPromptText()](#getPromptText) | Liest den Eingabetext (den Titel des Eingabefensters). |
| [getResult()](#getResult) | Ermittelt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [getSeparator()](#getSeparator) | Ermittelt den Knoten, der das Feldtrennzeichen darstellt. |
| [getStart()](#getStart) | Ermittelt den Knoten, der den Beginn des Feldes darstellt. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Ermittelt den Microsoft‑Word‑Feldtyp. |
| [isDirty()](#isDirty) | Ermittelt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [isDirty(boolean value)](#isDirty-boolean) | Legt fest, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [isLocked()](#isLocked) | Ermittelt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [isLocked(boolean value)](#isLocked-boolean) | Legt fest, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [remove()](#remove) | Entfernt das Feld aus dem Dokument. |
| [setDefaultResponse(String value)](#setDefaultResponse-java.lang.String) | Setzt die Standardantwort des Benutzers (Anfangswert im Eingabefenster). |
| [setLocaleId(int value)](#setLocaleId-int) | Legt die LCID des Feldes fest. |
| [setPromptOnceOnMailMerge(boolean value)](#setPromptOnceOnMailMerge-boolean) | Setzt, ob die Benutzerantwort pro Seriendruckvorgang einmal empfangen werden soll. |
| [setPromptText(String value)](#setPromptText-java.lang.String) | Setzt den Eingabetext (den Titel des Eingabefensters). |
| [setResult(String value)](#setResult-java.lang.String) | Setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [unlink()](#unlink) | Führt das Trennen des Feldes aus. |
| [update()](#update) | Führt die Feldaktualisierung aus. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Führt eine Feldaktualisierung aus. |
### getDefaultResponse() {#getDefaultResponse}
```
public String getDefaultResponse()
```


Liest die Standardantwort des Benutzers (Anfangswert im Eingabefenster).

 **Examples:** 

Zeigt, wie das FILLIN‑Feld verwendet wird, um den Benutzer zu einer Antwort aufzufordern.

```

 public void fieldFillIn() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a FILLIN field. When we manually update this field in Microsoft Word,
     // it will prompt us to enter a response. The field will then display the response as text.
     FieldFillIn field = (FieldFillIn) builder.insertField(FieldType.FIELD_FILL_IN, true);
     field.setPromptText("Please enter a response:");
     field.setDefaultResponse("A default response.");

     // We can also use these fields to ask the user for a unique response for each page
     // created during a mail merge done using Microsoft Word.
     field.setPromptOnceOnMailMerge(true);

     Assert.assertEquals(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.getFieldCode());

     FieldMergeField mergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     mergeField.setFieldName("MergeField");

     // If we perform a mail merge programmatically, we can use a custom prompt respondent
     // to automatically edit responses for FILLIN fields that the mail merge encounters.
     doc.getFieldOptions().setUserPromptRespondent(new PromptRespondent());
     doc.getMailMerge().execute(new String[]{"MergeField"}, new Object[]{""});

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.FILLIN.docx");
 }

 /// 
 /// Prepends a line to the default response of every FILLIN field during a mail merge.
 /// 
 private static class PromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response modified by PromptRespondent. " + defaultResponse;
     }
 }
 
```

**Returns:**
java.lang.String - Standardantwort des Benutzers (Anfangswert im Eingabefenster).
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
### getPromptOnceOnMailMerge() {#getPromptOnceOnMailMerge}
```
public boolean getPromptOnceOnMailMerge()
```


Liest, ob die Benutzerantwort pro Seriendruckvorgang einmal empfangen werden soll.

 **Examples:** 

Zeigt, wie das FILLIN‑Feld verwendet wird, um den Benutzer zu einer Antwort aufzufordern.

```

 public void fieldFillIn() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a FILLIN field. When we manually update this field in Microsoft Word,
     // it will prompt us to enter a response. The field will then display the response as text.
     FieldFillIn field = (FieldFillIn) builder.insertField(FieldType.FIELD_FILL_IN, true);
     field.setPromptText("Please enter a response:");
     field.setDefaultResponse("A default response.");

     // We can also use these fields to ask the user for a unique response for each page
     // created during a mail merge done using Microsoft Word.
     field.setPromptOnceOnMailMerge(true);

     Assert.assertEquals(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.getFieldCode());

     FieldMergeField mergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     mergeField.setFieldName("MergeField");

     // If we perform a mail merge programmatically, we can use a custom prompt respondent
     // to automatically edit responses for FILLIN fields that the mail merge encounters.
     doc.getFieldOptions().setUserPromptRespondent(new PromptRespondent());
     doc.getMailMerge().execute(new String[]{"MergeField"}, new Object[]{""});

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.FILLIN.docx");
 }

 /// 
 /// Prepends a line to the default response of every FILLIN field during a mail merge.
 /// 
 private static class PromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response modified by PromptRespondent. " + defaultResponse;
     }
 }
 
```

**Returns:**
boolean - Ob die Benutzerantwort pro Seriendruckvorgang einmal empfangen werden soll.
### getPromptText() {#getPromptText}
```
public String getPromptText()
```


Liest den Eingabetext (den Titel des Eingabefensters).

 **Examples:** 

Zeigt, wie das FILLIN‑Feld verwendet wird, um den Benutzer zu einer Antwort aufzufordern.

```

 public void fieldFillIn() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a FILLIN field. When we manually update this field in Microsoft Word,
     // it will prompt us to enter a response. The field will then display the response as text.
     FieldFillIn field = (FieldFillIn) builder.insertField(FieldType.FIELD_FILL_IN, true);
     field.setPromptText("Please enter a response:");
     field.setDefaultResponse("A default response.");

     // We can also use these fields to ask the user for a unique response for each page
     // created during a mail merge done using Microsoft Word.
     field.setPromptOnceOnMailMerge(true);

     Assert.assertEquals(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.getFieldCode());

     FieldMergeField mergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     mergeField.setFieldName("MergeField");

     // If we perform a mail merge programmatically, we can use a custom prompt respondent
     // to automatically edit responses for FILLIN fields that the mail merge encounters.
     doc.getFieldOptions().setUserPromptRespondent(new PromptRespondent());
     doc.getMailMerge().execute(new String[]{"MergeField"}, new Object[]{""});

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.FILLIN.docx");
 }

 /// 
 /// Prepends a line to the default response of every FILLIN field during a mail merge.
 /// 
 private static class PromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response modified by PromptRespondent. " + defaultResponse;
     }
 }
 
```

**Returns:**
java.lang.String - Der Eingabetext (der Titel des Eingabefensters).
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
### setDefaultResponse(String value) {#setDefaultResponse-java.lang.String}
```
public void setDefaultResponse(String value)
```


Setzt die Standardantwort des Benutzers (Anfangswert im Eingabefenster).

 **Examples:** 

Zeigt, wie das FILLIN‑Feld verwendet wird, um den Benutzer zu einer Antwort aufzufordern.

```

 public void fieldFillIn() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a FILLIN field. When we manually update this field in Microsoft Word,
     // it will prompt us to enter a response. The field will then display the response as text.
     FieldFillIn field = (FieldFillIn) builder.insertField(FieldType.FIELD_FILL_IN, true);
     field.setPromptText("Please enter a response:");
     field.setDefaultResponse("A default response.");

     // We can also use these fields to ask the user for a unique response for each page
     // created during a mail merge done using Microsoft Word.
     field.setPromptOnceOnMailMerge(true);

     Assert.assertEquals(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.getFieldCode());

     FieldMergeField mergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     mergeField.setFieldName("MergeField");

     // If we perform a mail merge programmatically, we can use a custom prompt respondent
     // to automatically edit responses for FILLIN fields that the mail merge encounters.
     doc.getFieldOptions().setUserPromptRespondent(new PromptRespondent());
     doc.getMailMerge().execute(new String[]{"MergeField"}, new Object[]{""});

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.FILLIN.docx");
 }

 /// 
 /// Prepends a line to the default response of every FILLIN field during a mail merge.
 /// 
 private static class PromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response modified by PromptRespondent. " + defaultResponse;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Standardbenutzerantwort (ursprünglicher Wert im Eingabeaufforderungsfenster enthalten). |

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

### setPromptOnceOnMailMerge(boolean value) {#setPromptOnceOnMailMerge-boolean}
```
public void setPromptOnceOnMailMerge(boolean value)
```


Setzt, ob die Benutzerantwort pro Seriendruckvorgang einmal empfangen werden soll.

 **Examples:** 

Zeigt, wie das FILLIN‑Feld verwendet wird, um den Benutzer zu einer Antwort aufzufordern.

```

 public void fieldFillIn() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a FILLIN field. When we manually update this field in Microsoft Word,
     // it will prompt us to enter a response. The field will then display the response as text.
     FieldFillIn field = (FieldFillIn) builder.insertField(FieldType.FIELD_FILL_IN, true);
     field.setPromptText("Please enter a response:");
     field.setDefaultResponse("A default response.");

     // We can also use these fields to ask the user for a unique response for each page
     // created during a mail merge done using Microsoft Word.
     field.setPromptOnceOnMailMerge(true);

     Assert.assertEquals(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.getFieldCode());

     FieldMergeField mergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     mergeField.setFieldName("MergeField");

     // If we perform a mail merge programmatically, we can use a custom prompt respondent
     // to automatically edit responses for FILLIN fields that the mail merge encounters.
     doc.getFieldOptions().setUserPromptRespondent(new PromptRespondent());
     doc.getMailMerge().execute(new String[]{"MergeField"}, new Object[]{""});

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.FILLIN.docx");
 }

 /// 
 /// Prepends a line to the default response of every FILLIN field during a mail merge.
 /// 
 private static class PromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response modified by PromptRespondent. " + defaultResponse;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob die Benutzerantwort einmal pro Seriendruckvorgang empfangen werden soll. |

### setPromptText(String value) {#setPromptText-java.lang.String}
```
public void setPromptText(String value)
```


Setzt den Eingabetext (den Titel des Eingabefensters).

 **Examples:** 

Zeigt, wie das FILLIN‑Feld verwendet wird, um den Benutzer zu einer Antwort aufzufordern.

```

 public void fieldFillIn() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a FILLIN field. When we manually update this field in Microsoft Word,
     // it will prompt us to enter a response. The field will then display the response as text.
     FieldFillIn field = (FieldFillIn) builder.insertField(FieldType.FIELD_FILL_IN, true);
     field.setPromptText("Please enter a response:");
     field.setDefaultResponse("A default response.");

     // We can also use these fields to ask the user for a unique response for each page
     // created during a mail merge done using Microsoft Word.
     field.setPromptOnceOnMailMerge(true);

     Assert.assertEquals(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.getFieldCode());

     FieldMergeField mergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     mergeField.setFieldName("MergeField");

     // If we perform a mail merge programmatically, we can use a custom prompt respondent
     // to automatically edit responses for FILLIN fields that the mail merge encounters.
     doc.getFieldOptions().setUserPromptRespondent(new PromptRespondent());
     doc.getMailMerge().execute(new String[]{"MergeField"}, new Object[]{""});

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.FILLIN.docx");
 }

 /// 
 /// Prepends a line to the default response of every FILLIN field during a mail merge.
 /// 
 private static class PromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response modified by PromptRespondent. " + defaultResponse;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Eingabetext (der Titel des Eingabeaufforderungsfensters). |

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

