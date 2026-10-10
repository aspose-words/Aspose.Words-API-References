---
title: "IFieldMergingCallback"
linktitle: "IFieldMergingCallback"
second_title: "Aspose.Words para Java"
description: "Implemente esta interfaz si desea controlar cómo se insertan los datos en los campos de combinación durante una operación de combinación de correspondencia en Java."
type: docs
weight: 765
url: /es/java/com.aspose.words/ifieldmergingcallback/
---
```
public interface IFieldMergingCallback
```

Implemente esta interfaz si desea controlar cómo se insertan datos en los campos de combinación durante una operación de combinación de correspondencia.

 **Examples:** 

Muestra cómo ejecutar una combinación de correspondencia con una devolución de llamada personalizada que maneja los datos de combinación en forma de documentos HTML.

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

Muestra cómo insertar imágenes almacenadas en un campo BLOB de base de datos en un informe.

```

 public void imageFromBlob() throws Exception {
     Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

     // Set up the event handler for image fields
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeImageFieldFromBlob());

     // Loads the driver
     Class.forName("net.ucanaccess.jdbc.UcanaccessDriver");

     // Open the database connection
     String connString = "jdbc:ucanaccess://" + getDatabaseDir() + "Northwind.accdb";

     // DSN-less DB connection
     java.sql.Connection conn = java.sql.DriverManager.getConnection(connString, "Admin", "");

     // Create and execute a command
     java.sql.Statement statement = conn.createStatement();
     java.sql.ResultSet resultSet = statement.executeQuery("SELECT * FROM Employees");

     DataTable table = new DataTable(resultSet, "Employees");

     // Perform mail merge
     doc.getMailMerge().executeWithRegions(table);

     // Close the database
     conn.close();

     doc.save(getArtifactsDir() + "MailMergeEvent.ImageFromBlob.docx");
 }

 private class HandleMergeImageFieldFromBlob implements IFieldMergingCallback {
     public void fieldMerging(final FieldMergingArgs args) {
         // Do nothing
     }

     // This is called when mail merge engine encounters Image:XXX merge field in the document.
     // You have a chance to return an Image object, file name or a stream that contains the image.
     public void imageFieldMerging(final ImageFieldMergingArgs e) {
         // The field value is a byte array, just cast it and create a stream on it
         ByteArrayInputStream imageStream = new ByteArrayInputStream((byte[]) e.getFieldValue());
         // Now the mail merge engine will retrieve the image from the stream
         e.setImageStream(imageStream);
     }
 }
 
```
## Métodos

| Método | Descripción |
| --- | --- |
| [fieldMerging(FieldMergingArgs args)](#fieldMerging-com.aspose.words.FieldMergingArgs) | Se llama cuando el motor de combinación de correspondencia de Aspose.Words está a punto de insertar datos en un campo de combinación en el documento. |
| [imageFieldMerging(ImageFieldMergingArgs args)](#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs) | Se llama cuando el motor de combinación de correspondencia de Aspose.Words está a punto de insertar una imagen en un campo de combinación. |
### fieldMerging(FieldMergingArgs args) {#fieldMerging-com.aspose.words.FieldMergingArgs}
```
public abstract void fieldMerging(FieldMergingArgs args)
```


Se llama cuando el motor de combinación de correspondencia de Aspose.Words está a punto de insertar datos en un campo de combinación en el documento.

 **Examples:** 

Muestra cómo ejecutar una combinación de correspondencia con una devolución de llamada personalizada que maneja los datos de combinación en forma de documentos HTML.

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

Muestra cómo insertar imágenes almacenadas en un campo BLOB de base de datos en un informe.

```

 public void imageFromBlob() throws Exception {
     Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

     // Set up the event handler for image fields
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeImageFieldFromBlob());

     // Loads the driver
     Class.forName("net.ucanaccess.jdbc.UcanaccessDriver");

     // Open the database connection
     String connString = "jdbc:ucanaccess://" + getDatabaseDir() + "Northwind.accdb";

     // DSN-less DB connection
     java.sql.Connection conn = java.sql.DriverManager.getConnection(connString, "Admin", "");

     // Create and execute a command
     java.sql.Statement statement = conn.createStatement();
     java.sql.ResultSet resultSet = statement.executeQuery("SELECT * FROM Employees");

     DataTable table = new DataTable(resultSet, "Employees");

     // Perform mail merge
     doc.getMailMerge().executeWithRegions(table);

     // Close the database
     conn.close();

     doc.save(getArtifactsDir() + "MailMergeEvent.ImageFromBlob.docx");
 }

 private class HandleMergeImageFieldFromBlob implements IFieldMergingCallback {
     public void fieldMerging(final FieldMergingArgs args) {
         // Do nothing
     }

     // This is called when mail merge engine encounters Image:XXX merge field in the document.
     // You have a chance to return an Image object, file name or a stream that contains the image.
     public void imageFieldMerging(final ImageFieldMergingArgs e) {
         // The field value is a byte array, just cast it and create a stream on it
         ByteArrayInputStream imageStream = new ByteArrayInputStream((byte[]) e.getFieldValue());
         // Now the mail merge engine will retrieve the image from the stream
         e.setImageStream(imageStream);
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| args | [FieldMergingArgs](../../com.aspose.words/fieldmergingargs/) |  |

### imageFieldMerging(ImageFieldMergingArgs args) {#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs}
```
public abstract void imageFieldMerging(ImageFieldMergingArgs args)
```


Se llama cuando el motor de combinación de correspondencia de Aspose.Words está a punto de insertar una imagen en un campo de combinación.

 **Examples:** 

Muestra cómo insertar imágenes almacenadas en un campo BLOB de base de datos en un informe.

```

 public void imageFromBlob() throws Exception {
     Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

     // Set up the event handler for image fields
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeImageFieldFromBlob());

     // Loads the driver
     Class.forName("net.ucanaccess.jdbc.UcanaccessDriver");

     // Open the database connection
     String connString = "jdbc:ucanaccess://" + getDatabaseDir() + "Northwind.accdb";

     // DSN-less DB connection
     java.sql.Connection conn = java.sql.DriverManager.getConnection(connString, "Admin", "");

     // Create and execute a command
     java.sql.Statement statement = conn.createStatement();
     java.sql.ResultSet resultSet = statement.executeQuery("SELECT * FROM Employees");

     DataTable table = new DataTable(resultSet, "Employees");

     // Perform mail merge
     doc.getMailMerge().executeWithRegions(table);

     // Close the database
     conn.close();

     doc.save(getArtifactsDir() + "MailMergeEvent.ImageFromBlob.docx");
 }

 private class HandleMergeImageFieldFromBlob implements IFieldMergingCallback {
     public void fieldMerging(final FieldMergingArgs args) {
         // Do nothing
     }

     // This is called when mail merge engine encounters Image:XXX merge field in the document.
     // You have a chance to return an Image object, file name or a stream that contains the image.
     public void imageFieldMerging(final ImageFieldMergingArgs e) {
         // The field value is a byte array, just cast it and create a stream on it
         ByteArrayInputStream imageStream = new ByteArrayInputStream((byte[]) e.getFieldValue());
         // Now the mail merge engine will retrieve the image from the stream
         e.setImageStream(imageStream);
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| args | [ImageFieldMergingArgs](../../com.aspose.words/imagefieldmergingargs/) |  |

