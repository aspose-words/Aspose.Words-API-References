---
title: "IFieldUserPromptRespondent"
linktitle: "IFieldUserPromptRespondent"
second_title: "Aspose.Words para Java"
description: "Representa al respondedor de indicaciones del usuario durante la actualización de campos en Java."
type: docs
weight: 770
url: /es/java/com.aspose.words/ifielduserpromptrespondent/
---
```
public interface IFieldUserPromptRespondent
```

Representa al respondedor de los mensajes al usuario durante la actualización del campo.

 **Remarks:** 

Los campos ASK y FILLIN son ejemplos de campos que solicitan al usuario una respuesta. Implemente esta interfaz y asígnela a la propiedad [FieldOptions.getUserPromptRespondent()](../../com.aspose.words/fieldoptions/\#getUserPromptRespondent) / [FieldOptions.setUserPromptRespondent(com.aspose.words.IFieldUserPromptRespondent)](../../com.aspose.words/fieldoptions/\#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent) para establecer la interacción entre la actualización del campo y el usuario.

 **Examples:** 

Muestra cómo crear un campo ASK y establecer sus propiedades.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [respond(String promptText, String defaultResponse)](#respond-java.lang.String-java.lang.String) | Cuando se implementa, devuelve una respuesta del usuario al solicitar. |
### respond(String promptText, String defaultResponse) {#respond-java.lang.String-java.lang.String}
```
public abstract String respond(String promptText, String defaultResponse)
```


Cuando se implementa, devuelve una respuesta del usuario al solicitar. Su implementación debe devolver  null  para indicar que el usuario no ha respondido al mensaje (es decir, el usuario ha pulsado el botón Cancelar en la ventana del mensaje).

 **Examples:** 

Muestra cómo crear un campo ASK y establecer sus propiedades.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| promptText | java.lang.String | Texto del mensaje (es decir, título de la ventana del mensaje). |
| defaultResponse | java.lang.String | Respuesta predeterminada del usuario (es decir, valor inicial contenido en la ventana del mensaje). |

**Returns:**
java.lang.String - Respuesta del usuario (es decir, valor confirmado contenido en la ventana del mensaje).
