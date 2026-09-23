---
title: "FieldMergingArgs"
linktitle: "FieldMergingArgs"
second_title: "Aspose.Words per Java"
description: "Fornisce dati per l'evento MergeField in Java."
type: docs
weight: 261
url: /it/java/com.aspose.words/fieldmergingargs/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase/)
```
public class FieldMergingArgs extends FieldMergingArgsBase
```

Fornisce dati per l'evento **MergeField**.

Per saperne di più, visita l'articolo di documentazione [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

L'evento **MergeField** si verifica durante l'unione della posta quando nel documento viene incontrato un semplice campo di unione della posta. È possibile rispondere a questo evento per restituire del testo che il motore di unione della posta inserirà nel documento.

 **Examples:** 

Mostra come eseguire una stampa unione con un callback personalizzato che gestisce i dati di unione sotto forma di documenti HTML.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getDocument()](#getDocument) | Restituisce l'oggetto [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) per il quale viene eseguita la mail merge. |
| [getDocumentFieldName()](#getDocumentFieldName) | Ottiene il nome del campo di unione così come specificato nel documento. |
| [getField()](#getField) | Ottiene l'oggetto che rappresenta il campo di unione corrente. |
| [getFieldName()](#getFieldName) | Ottiene il nome del campo di unione nella fonte dati. |
| [getFieldValue()](#getFieldValue) | Ottiene il valore del campo dalla fonte dati. |
| [getRecordIndex()](#getRecordIndex) | Ottiene l'indice basato su zero del record che viene unito. |
| [getTableName()](#getTableName) | Ottiene il nome della tabella dati per l'operazione di unione corrente o una stringa vuota se il nome non è disponibile. |
| [getText()](#getText) | Ottiene il testo che verrà inserito nel documento per il campo di unione corrente. |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object) | Imposta il valore del campo dalla fonte dati. |
| [setText(String value)](#setText-java.lang.String) | Imposta il testo che verrà inserito nel documento per il campo di unione corrente. |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Restituisce l'oggetto [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) per il quale viene eseguita la mail merge.

 **Examples:** 

Mostra come eseguire una stampa unione con un callback personalizzato che gestisce i dati di unione sotto forma di documenti HTML.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) object for which the mail merge is performed.
### getDocumentFieldName() {#getDocumentFieldName}
```
public String getDocumentFieldName()
```


Ottiene il nome del campo di unione così come specificato nel documento.

 **Remarks:** 

Se hai una mappatura dal nome del campo del documento a un nome di campo diverso nella fonte dati, questo è il nome originale del campo così come specificato nel documento.

Se hai specificato un prefisso per il nome del campo, ad esempio "Image:MyFieldName" nel documento, allora [getDocumentFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getDocumentFieldName) restituisce il nome del campo senza il prefisso, cioè "MyFieldName".

 **Examples:** 

Mostra come eseguire una stampa unione con un callback personalizzato che gestisce i dati di unione sotto forma di documenti HTML.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

**Returns:**
java.lang.String - Il nome del campo di unione così come specificato nel documento.
### getField() {#getField}
```
public FieldMergeField getField()
```


Ottiene l'oggetto che rappresenta il campo di unione corrente.

 **Examples:** 

Mostra come eseguire una stampa unione con un callback personalizzato che gestisce i dati di unione sotto forma di documenti HTML.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

**Returns:**
[FieldMergeField](../../com.aspose.words/fieldmergefield/) - The object that represents the current merge field.
### getFieldName() {#getFieldName}
```
public String getFieldName()
```


Ottiene il nome del campo di unione nella fonte dati.

 **Remarks:** 

Se hai una mappatura dal nome del campo del documento a un nome di campo diverso nella fonte dati, questo è il nome del campo mappato.

Se hai specificato un prefisso per il nome del campo, ad esempio "Image:MyFieldName" nel documento, allora [getFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getFieldName) restituisce il nome del campo senza il prefisso, cioè "MyFieldName".

 **Examples:** 

Mostra come inserire campi di modulo checkbox in un documento durante la mail merge.

```

 public void insertCheckBox() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startTable();
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableStart:StudentCourse ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  CourseName ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableEnd:StudentCourse ");
     builder.endTable();

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertCheckBox());

     // Execute mail merge with regions
     DataTable dataTable = getStudentCourseDataTable();
     doc.getMailMerge().executeWithRegions(dataTable);

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertCheckBox.docx");
 }

 private class HandleMergeFieldInsertCheckBox implements IFieldMergingCallback {
     // This is called for each merge field in the document
     // when Document.MailMerge.ExecuteWithRegions is called.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         if (args.getDocumentFieldName().equals("CourseName")) {
             // The name of the table that we are merging can be found here
             Assert.assertEquals(args.getTableName(), "StudentCourse");

             // Insert the checkbox for this merge field, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getFieldName());
             builder.insertCheckBox(args.getDocumentFieldName() + mCheckBoxCount, false, 0);
             // Get the actual value of the field
             String fieldValue = args.getFieldValue().toString();

             // In this case, for every record index 'n', the corresponding field value is "Course n"
             Assert.assertEquals(args.getRecordIndex(), Character.getNumericValue(fieldValue.charAt(7)));

             builder.write(fieldValue);
             mCheckBoxCount++;
         }
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         // Do nothing
     }

     // Counter for CheckBox name generation.
     private int mCheckBoxCount;
 }

 // Create DataTable and fill it with data.
 // In real life this DataTable should be filled from a database.
 private static DataTable getStudentCourseDataTable() throws Exception {
     DataTable dataTable = new DataTable("StudentCourse");
     dataTable.getColumns().add("CourseName");
     for (int i = 0; i < 10; i++) {
         DataRow datarow = dataTable.newRow();
         dataTable.getRows().add(datarow);
         datarow.set(0, "Course " + i);
     }
     return dataTable;
 }
 
```

**Returns:**
java.lang.String - Il nome del campo di unione nella fonte dati.
### getFieldValue() {#getFieldValue}
```
public Object getFieldValue()
```


Ottiene il valore del campo dalla fonte dati.

 **Remarks:** 

Questa proprietà contiene un valore appena selezionato dalla tua fonte dati per questo campo dal motore di mail merge. Puoi anche sostituire il valore impostando la proprietà.

 **Examples:** 

Mostra come utilizzare il valore della fonte dati del campo.

```

 public void fieldFormats() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField("MERGEFIELD TextField \\* Caps", null);
     builder.write(", ");
     builder.insertField("MERGEFIELD TextField2 \\* Upper", null);
     builder.write(", ");
     builder.insertField("MERGEFIELD NumericField \\# 0.0", null);

     builder.getDocument().getMailMerge().setFieldMergingCallback(new FieldValueMergingCallback());

     builder.getDocument().getMailMerge().execute(
             new String[]{"TextField", "TextField2", "NumericField"},
             new Object[]{"Original value", "Original value", 10});

     Assert.assertEquals("New Value, New value from FieldMergingArgs, 20.0", doc.getText().trim());
 }

 private static class FieldValueMergingCallback implements IFieldMergingCallback {
     /// 
     /// This is called when merge field is actually merged with data in the document.
     /// 
     public void fieldMerging(FieldMergingArgs e) {
         switch (e.getFieldName()) {
             case "TextField":
                 Assert.assertEquals("Original value", e.getFieldValue());
                 e.setFieldValue("New value");
                 break;
             case "TextField2":
                 Assert.assertEquals("Original value", e.getFieldValue());
                 e.setText("New value from FieldMergingArgs");   // Should suppress e.FieldValue and ignore format
                 e.setFieldValue("new value");
                 break;
             case "NumericField":
                 Assert.assertEquals(10, e.getFieldValue());
                 e.setFieldValue(20);
                 break;
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs e) {
         // Do nothing
     }
 }
 
```

**Returns:**
java.lang.Object - Il valore del campo dalla fonte dati.
### getRecordIndex() {#getRecordIndex}
```
public int getRecordIndex()
```


Ottiene l'indice basato su zero del record che viene unito.

 **Examples:** 

Mostra come inserire campi di modulo checkbox in un documento durante la mail merge.

```

 public void insertCheckBox() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startTable();
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableStart:StudentCourse ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  CourseName ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableEnd:StudentCourse ");
     builder.endTable();

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertCheckBox());

     // Execute mail merge with regions
     DataTable dataTable = getStudentCourseDataTable();
     doc.getMailMerge().executeWithRegions(dataTable);

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertCheckBox.docx");
 }

 private class HandleMergeFieldInsertCheckBox implements IFieldMergingCallback {
     // This is called for each merge field in the document
     // when Document.MailMerge.ExecuteWithRegions is called.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         if (args.getDocumentFieldName().equals("CourseName")) {
             // The name of the table that we are merging can be found here
             Assert.assertEquals(args.getTableName(), "StudentCourse");

             // Insert the checkbox for this merge field, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getFieldName());
             builder.insertCheckBox(args.getDocumentFieldName() + mCheckBoxCount, false, 0);
             // Get the actual value of the field
             String fieldValue = args.getFieldValue().toString();

             // In this case, for every record index 'n', the corresponding field value is "Course n"
             Assert.assertEquals(args.getRecordIndex(), Character.getNumericValue(fieldValue.charAt(7)));

             builder.write(fieldValue);
             mCheckBoxCount++;
         }
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         // Do nothing
     }

     // Counter for CheckBox name generation.
     private int mCheckBoxCount;
 }

 // Create DataTable and fill it with data.
 // In real life this DataTable should be filled from a database.
 private static DataTable getStudentCourseDataTable() throws Exception {
     DataTable dataTable = new DataTable("StudentCourse");
     dataTable.getColumns().add("CourseName");
     for (int i = 0; i < 10; i++) {
         DataRow datarow = dataTable.newRow();
         dataTable.getRows().add(datarow);
         datarow.set(0, "Course " + i);
     }
     return dataTable;
 }
 
```

**Returns:**
int - L'indice basato su zero del record che viene unito.
### getTableName() {#getTableName}
```
public String getTableName()
```


Ottiene il nome della tabella dati per l'operazione di unione corrente o una stringa vuota se il nome non è disponibile.

 **Examples:** 

Mostra come inserire campi di modulo checkbox in un documento durante la mail merge.

```

 public void insertCheckBox() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startTable();
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableStart:StudentCourse ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  CourseName ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableEnd:StudentCourse ");
     builder.endTable();

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertCheckBox());

     // Execute mail merge with regions
     DataTable dataTable = getStudentCourseDataTable();
     doc.getMailMerge().executeWithRegions(dataTable);

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertCheckBox.docx");
 }

 private class HandleMergeFieldInsertCheckBox implements IFieldMergingCallback {
     // This is called for each merge field in the document
     // when Document.MailMerge.ExecuteWithRegions is called.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         if (args.getDocumentFieldName().equals("CourseName")) {
             // The name of the table that we are merging can be found here
             Assert.assertEquals(args.getTableName(), "StudentCourse");

             // Insert the checkbox for this merge field, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getFieldName());
             builder.insertCheckBox(args.getDocumentFieldName() + mCheckBoxCount, false, 0);
             // Get the actual value of the field
             String fieldValue = args.getFieldValue().toString();

             // In this case, for every record index 'n', the corresponding field value is "Course n"
             Assert.assertEquals(args.getRecordIndex(), Character.getNumericValue(fieldValue.charAt(7)));

             builder.write(fieldValue);
             mCheckBoxCount++;
         }
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         // Do nothing
     }

     // Counter for CheckBox name generation.
     private int mCheckBoxCount;
 }

 // Create DataTable and fill it with data.
 // In real life this DataTable should be filled from a database.
 private static DataTable getStudentCourseDataTable() throws Exception {
     DataTable dataTable = new DataTable("StudentCourse");
     dataTable.getColumns().add("CourseName");
     for (int i = 0; i < 10; i++) {
         DataRow datarow = dataTable.newRow();
         dataTable.getRows().add(datarow);
         datarow.set(0, "Course " + i);
     }
     return dataTable;
 }
 
```

**Returns:**
java.lang.String - Il nome della tabella dati per l'operazione di unione corrente o stringa vuota se il nome non è disponibile.
### getText() {#getText}
```
public String getText()
```


Ottiene il testo che verrà inserito nel documento per il campo di unione corrente.

 **Remarks:** 

Quando il tuo gestore di eventi viene chiamato, questa proprietà è impostata su  null .

Se lasci Text impostato su  null , il motore di unione della posta inserirà [FieldMergingArgsBase.getFieldValue()](../../com.aspose.words/fieldmergingargsbase/\#getFieldValue) / [FieldMergingArgsBase.setFieldValue(java.lang.Object)](../../com.aspose.words/fieldmergingargsbase/\#setFieldValue-java.lang.Object) al posto del campo di unione.

Se imposti Text su qualsiasi stringa (inclusa quella vuota), la stringa verrà inserita nel documento al posto del campo di unione.

 **Examples:** 

Mostra come eseguire una stampa unione con un callback personalizzato che gestisce i dati di unione sotto forma di documenti HTML.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

**Returns:**
java.lang.String - Il testo che verrà inserito nel documento per il campo di unione corrente.
### setFieldValue(Object value) {#setFieldValue-java.lang.Object}
```
public void setFieldValue(Object value)
```


Imposta il valore del campo dalla fonte dati.

 **Remarks:** 

Questa proprietà contiene un valore appena selezionato dalla tua fonte dati per questo campo dal motore di mail merge. Puoi anche sostituire il valore impostando la proprietà.

 **Examples:** 

Mostra come utilizzare il valore della fonte dati del campo.

```

 public void fieldFormats() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField("MERGEFIELD TextField \\* Caps", null);
     builder.write(", ");
     builder.insertField("MERGEFIELD TextField2 \\* Upper", null);
     builder.write(", ");
     builder.insertField("MERGEFIELD NumericField \\# 0.0", null);

     builder.getDocument().getMailMerge().setFieldMergingCallback(new FieldValueMergingCallback());

     builder.getDocument().getMailMerge().execute(
             new String[]{"TextField", "TextField2", "NumericField"},
             new Object[]{"Original value", "Original value", 10});

     Assert.assertEquals("New Value, New value from FieldMergingArgs, 20.0", doc.getText().trim());
 }

 private static class FieldValueMergingCallback implements IFieldMergingCallback {
     /// 
     /// This is called when merge field is actually merged with data in the document.
     /// 
     public void fieldMerging(FieldMergingArgs e) {
         switch (e.getFieldName()) {
             case "TextField":
                 Assert.assertEquals("Original value", e.getFieldValue());
                 e.setFieldValue("New value");
                 break;
             case "TextField2":
                 Assert.assertEquals("Original value", e.getFieldValue());
                 e.setText("New value from FieldMergingArgs");   // Should suppress e.FieldValue and ignore format
                 e.setFieldValue("new value");
                 break;
             case "NumericField":
                 Assert.assertEquals(10, e.getFieldValue());
                 e.setFieldValue(20);
                 break;
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs e) {
         // Do nothing
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.Object | Il valore del campo dalla fonte dati. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Imposta il testo che verrà inserito nel documento per il campo di unione corrente.

 **Remarks:** 

Quando il tuo gestore di eventi viene chiamato, questa proprietà è impostata su  null .

Se lasci Text impostato su  null , il motore di unione della posta inserirà [FieldMergingArgsBase.getFieldValue()](../../com.aspose.words/fieldmergingargsbase/\#getFieldValue) / [FieldMergingArgsBase.setFieldValue(java.lang.Object)](../../com.aspose.words/fieldmergingargsbase/\#setFieldValue-java.lang.Object) al posto del campo di unione.

Se imposti Text su qualsiasi stringa (inclusa quella vuota), la stringa verrà inserita nel documento al posto del campo di unione.

 **Examples:** 

Mostra come eseguire una stampa unione con un callback personalizzato che gestisce i dati di unione sotto forma di documenti HTML.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il testo che verrà inserito nel documento per il campo di unione corrente. |

