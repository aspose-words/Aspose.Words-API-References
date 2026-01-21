---
title: FieldMergingArgsBase
linktitle: FieldMergingArgsBase
second_title: Aspose.Words for Java
description: Base class for FieldMergingArgs and ImageFieldMergingArgs in Java.
type: docs
weight: 262
url: /java/com.aspose.words/fieldmergingargsbase/
---

**Inheritance:**
java.lang.Object
```
public abstract class FieldMergingArgsBase
```

Base class for [FieldMergingArgs](../../com.aspose.words/fieldmergingargs/) and [ImageFieldMergingArgs](../../com.aspose.words/imagefieldmergingargs/).

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

 **Remarks:** 

 **Examples:** 

Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [FieldMergingArgsBase()](#FieldMergingArgsBase) |  |
## Methods

| Method | Description |
| --- | --- |
| [getDocument()](#getDocument) | Returns the [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) object for which the mail merge is performed. |
| [getDocumentFieldName()](#getDocumentFieldName) | Gets the name of the merge field as specified in the document. |
| [getField()](#getField) | Gets the object that represents the current merge field. |
| [getFieldName()](#getFieldName) | Gets the name of the merge field in the data source. |
| [getFieldValue()](#getFieldValue) | Gets the value of the field from the data source. |
| [getRecordIndex()](#getRecordIndex) | Gets the zero based index of the record that is being merged. |
| [getTableName()](#getTableName) | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object) | Sets the value of the field from the data source. |
### FieldMergingArgsBase() {#FieldMergingArgsBase}
```
public FieldMergingArgsBase()
```


### getDocument() {#getDocument}
```
public Document getDocument()
```


Returns the [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) object for which the mail merge is performed.

 **Examples:** 

Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents.

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


Gets the name of the merge field as specified in the document.

 **Remarks:** 

If you have a mapping from a document field name to a different data source field name, then this is the original field name as specified in the document.

If you specified a field name prefix, for example "Image:MyFieldName" in the document, then [getDocumentFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getDocumentFieldName) returns field name without the prefix, that is "MyFieldName".

 **Examples:** 

Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents.

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
java.lang.String - The name of the merge field as specified in the document.
### getField() {#getField}
```
public FieldMergeField getField()
```


Gets the object that represents the current merge field.

 **Examples:** 

Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents.

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


Gets the name of the merge field in the data source.

 **Remarks:** 

If you have a mapping from a document field name to a different data source field name, then this is the mapped field name.

If you specified a field name prefix, for example "Image:MyFieldName" in the document, then [getFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getFieldName) returns field name without the prefix, that is "MyFieldName".

 **Examples:** 

Shows how to insert checkbox form fields into a document during mail merge.

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
java.lang.String - The name of the merge field in the data source.
### getFieldValue() {#getFieldValue}
```
public Object getFieldValue()
```


Gets the value of the field from the data source.

 **Remarks:** 

This property contains a value that has just been selected from your data source for this field by the mail merge engine. You can also replace the value by setting the property.

 **Examples:** 

Shows how to use data source value of the field.

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
java.lang.Object - The value of the field from the data source.
### getRecordIndex() {#getRecordIndex}
```
public int getRecordIndex()
```


Gets the zero based index of the record that is being merged.

 **Examples:** 

Shows how to insert checkbox form fields into a document during mail merge.

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
int - The zero based index of the record that is being merged.
### getTableName() {#getTableName}
```
public String getTableName()
```


Gets the name of the data table for the current merge operation or empty string if the name is not available.

 **Examples:** 

Shows how to insert checkbox form fields into a document during mail merge.

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
java.lang.String - The name of the data table for the current merge operation or empty string if the name is not available.
### setFieldValue(Object value) {#setFieldValue-java.lang.Object}
```
public void setFieldValue(Object value)
```


Sets the value of the field from the data source.

 **Remarks:** 

This property contains a value that has just been selected from your data source for this field by the mail merge engine. You can also replace the value by setting the property.

 **Examples:** 

Shows how to use data source value of the field.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Object | The value of the field from the data source. |

