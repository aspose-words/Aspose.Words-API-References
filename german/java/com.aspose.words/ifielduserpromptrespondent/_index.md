---
title: "IFieldUserPromptRespondent"
linktitle: "IFieldUserPromptRespondent"
second_title: "Aspose.Words für Java"
description: "Stellt den Befragten für Benutzer‑Eingabeaufforderungen während der Feldaktualisierung in Java dar."
type: docs
weight: 770
url: /de/java/com.aspose.words/ifielduserpromptrespondent/
---
```
public interface IFieldUserPromptRespondent
```

Stellt den Befragten für Benutzeraufforderungen während der Feldaktualisierung dar.

 **Remarks:** 

Die Felder ASK und FILLIN sind Beispiele für Felder, die den Benutzer zu einer Antwort auffordern. Implementieren Sie dieses Interface und weisen Sie es der Eigenschaft [FieldOptions.getUserPromptRespondent()](../../com.aspose.words/fieldoptions/\#getUserPromptRespondent) / [FieldOptions.setUserPromptRespondent(com.aspose.words.IFieldUserPromptRespondent)](../../com.aspose.words/fieldoptions/\#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent) zu, um die Interaktion zwischen Feldaktualisierung und dem Benutzer herzustellen.

 **Examples:** 

Zeigt, wie ein ASK-Feld erstellt und dessen Eigenschaften festgelegt werden.

```

 public void fieldAsk() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Place a field where the response to our ASK field will be placed.
     FieldRef fieldRef = (FieldRef) builder.insertField(FieldType.FIELD_REF, true);
     fieldRef.setBookmarkName("MyAskField");
     builder.writeln();

     Assert.assertEquals(" REF  MyAskField", fieldRef.getFieldCode());

     // Insert the ASK field and edit its properties to reference our REF field by bookmark name.
     FieldAsk fieldAsk = (FieldAsk) builder.insertField(FieldType.FIELD_ASK, true);
     fieldAsk.setBookmarkName("MyAskField");
     fieldAsk.setPromptText("Please provide a response for this ASK field");
     fieldAsk.setDefaultResponse("Response from within the field.");
     fieldAsk.setPromptOnceOnMailMerge(true);
     builder.writeln();

     Assert.assertEquals(
             " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
             fieldAsk.getFieldCode());

     // ASK fields apply the default response to their respective REF fields during a mail merge.
     DataTable table = new DataTable("My Table");
     table.getColumns().add("Column 1");
     table.getRows().add("Row 1");
     table.getRows().add("Row 2");

     FieldMergeField fieldMergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     fieldMergeField.setFieldName("Column 1");

     // We can modify or override the default response in our ASK fields with a custom prompt responder,
     // which will occur during a mail merge.
     doc.getFieldOptions().setUserPromptRespondent(new MyPromptRespondent());
     doc.getMailMerge().execute(table);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.ASK.docx");
 }

 /// 
 /// Prepends text to the default response of an ASK field during a mail merge.
 /// 
 private static class MyPromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response from MyPromptRespondent. " + defaultResponse;
     }
 }
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [respond(String promptText, String defaultResponse)](#respond-java.lang.String-java.lang.String) | Wenn implementiert, gibt sie eine Antwort des Benutzers auf die Eingabeaufforderung zurück. |
### respond(String promptText, String defaultResponse) {#respond-java.lang.String-java.lang.String}
```
public abstract String respond(String promptText, String defaultResponse)
```


Wenn implementiert, gibt sie eine Antwort des Benutzers auf die Eingabeaufforderung zurück. Ihre Implementierung sollte  null  zurückgeben, um anzuzeigen, dass der Benutzer nicht auf die Aufforderung reagiert hat (d. h. der Benutzer hat die Abbrechen‑Schaltfläche im Eingabeaufforderungsfenster gedrückt).

 **Examples:** 

Zeigt, wie ein ASK-Feld erstellt und dessen Eigenschaften festgelegt werden.

```

 public void fieldAsk() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Place a field where the response to our ASK field will be placed.
     FieldRef fieldRef = (FieldRef) builder.insertField(FieldType.FIELD_REF, true);
     fieldRef.setBookmarkName("MyAskField");
     builder.writeln();

     Assert.assertEquals(" REF  MyAskField", fieldRef.getFieldCode());

     // Insert the ASK field and edit its properties to reference our REF field by bookmark name.
     FieldAsk fieldAsk = (FieldAsk) builder.insertField(FieldType.FIELD_ASK, true);
     fieldAsk.setBookmarkName("MyAskField");
     fieldAsk.setPromptText("Please provide a response for this ASK field");
     fieldAsk.setDefaultResponse("Response from within the field.");
     fieldAsk.setPromptOnceOnMailMerge(true);
     builder.writeln();

     Assert.assertEquals(
             " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
             fieldAsk.getFieldCode());

     // ASK fields apply the default response to their respective REF fields during a mail merge.
     DataTable table = new DataTable("My Table");
     table.getColumns().add("Column 1");
     table.getRows().add("Row 1");
     table.getRows().add("Row 2");

     FieldMergeField fieldMergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     fieldMergeField.setFieldName("Column 1");

     // We can modify or override the default response in our ASK fields with a custom prompt responder,
     // which will occur during a mail merge.
     doc.getFieldOptions().setUserPromptRespondent(new MyPromptRespondent());
     doc.getMailMerge().execute(table);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.ASK.docx");
 }

 /// 
 /// Prepends text to the default response of an ASK field during a mail merge.
 /// 
 private static class MyPromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response from MyPromptRespondent. " + defaultResponse;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| promptText | java.lang.String | Aufforderungstext (d. h. Titel des Eingabeaufforderungsfensters). |
| defaultResponse | java.lang.String | Standardbenutzerantwort (d. h. Anfangswert, der im Eingabeaufforderungsfenster enthalten ist). |

**Returns:**
java.lang.String - Benutzerantwort (d. h. bestätigter Wert, der im Eingabeaufforderungsfenster enthalten ist).
