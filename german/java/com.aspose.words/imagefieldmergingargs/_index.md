---
title: "ImageFieldMergingArgs"
linktitle: "ImageFieldMergingArgs"
second_title: "Aspose.Words für Java"
description: "Stellt Daten für das Ereignis IFieldMergingCallback.imageFieldMergingcom.aspose.words.ImageFieldMergingArgs in Java bereit."
type: docs
weight: 392
url: /de/java/com.aspose.words/imagefieldmergingargs/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase/)
```
public class ImageFieldMergingArgs extends FieldMergingArgsBase
```

Stellt Daten für das Ereignis [IFieldMergingCallback.imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../../com.aspose.words/ifieldmergingcallback/\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs) bereit.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Dieses Ereignis tritt beim Seriendruck auf, wenn ein Bild‑Seriendruckfeld im Dokument gefunden wird. Sie können auf dieses Ereignis reagieren, indem Sie einen Dateinamen, einen Stream oder ein java.awt.image.BufferedImage‑Objekt an die Seriendruck‑Engine zurückgeben, damit es in das Dokument eingefügt wird.

Es stehen drei Eigenschaften zur Verfügung: [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String), **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** und [getImage()](../../com.aspose.words/imagefieldmergingargs/\#getImage) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs/\#setImage-java.awt.image.BufferedImage), um anzugeben, woher das Bild genommen werden soll. Setzen Sie nur eine dieser Eigenschaften.

Um ein Bild‑Seriendruckfeld in ein Word‑Dokument einzufügen, wählen Sie den Befehl Einfügen/Feld, dann MergeField und geben Sie Image:MyFieldName ein.

 **Examples:** 

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wie MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```

 public void mergeFieldImageDimension() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source containing local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // The data source should have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Create a suitable data source.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add(getImageDir() + "Logo.jpg");
     dataTable.getRows().add(getImageDir() + "Transparent background logo.png");
     dataTable.getRows().add(getImageDir() + "Enhanced Windows MetaFile.emf");

     // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new MergedImageResizer(200.0, 200.0, MergeFieldImageDimensionUnit.POINT));
     doc.getMailMerge().execute(dataTable);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.MERGEFIELD.ImageDimension.docx");
 }

 /// 
 /// Sets the size of all mail merged images to one defined width and height.
 /// 
 private static class MergedImageResizer implements IFieldMergingCallback {
     public MergedImageResizer(final double imageWidth, final double imageHeight, final int unit) {
         mImageWidth = imageWidth;
         mImageHeight = imageHeight;
         mUnit = unit;
     }

     public void fieldMerging(final FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         args.setImageFileName(args.getFieldValue().toString());
         args.setImageWidth(new MergeFieldImageDimension(mImageWidth, mUnit));
         args.setImageHeight(new MergeFieldImageDimension(mImageHeight, mUnit));

         Assert.assertEquals(mImageWidth, args.getImageWidth().getValue());
         Assert.assertEquals(mUnit, args.getImageWidth().getUnit());
         Assert.assertEquals(mImageHeight, args.getImageHeight().getValue());
         Assert.assertEquals(mUnit, args.getImageHeight().getUnit());
         Assert.assertNull(args.getShape());
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

Zeigt, wie Bilder, die in einem Datenbank‑BLOB‑Feld gespeichert sind, in einen Bericht eingefügt werden.

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


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getDocument()](#getDocument) | Gibt das [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument)-Objekt zurück, für das der Seriendruck ausgeführt wird. |
| [getDocumentFieldName()](#getDocumentFieldName) | Liefert den Namen des Seriendruckfeldes, wie im Dokument angegeben. |
| [getField()](#getField) | Liefert das Objekt, das das aktuelle Seriendruckfeld repräsentiert. |
| [getFieldName()](#getFieldName) | Liefert den Namen des Seriendruckfeldes in der Datenquelle. |
| [getFieldValue()](#getFieldValue) | Liefert den Wert des Feldes aus der Datenquelle. |
| [getImage()](#getImage) | Gibt das Bild an, das die Seriendruck‑Engine in das Dokument einfügen muss. |
| [getImageFileName()](#getImageFileName) | Legt den Dateinamen des Bildes fest, das die Seriendruck‑Engine in das Dokument einfügen muss. |
| [getImageHeight()](#getImageHeight) | Gibt die Bildhöhe für das in das Dokument einzufügende Bild an. |
| [getImageStream()](#getImageStream) |  |
| [getImageWidth()](#getImageWidth) | Gibt die Bildbreite für das in das Dokument einzufügende Bild an. |
| [getRecordIndex()](#getRecordIndex) | Liefert den nullbasierten Index des Datensatzes, der zusammengeführt wird. |
| [getShape()](#getShape) | Gibt die Form an, die die Seriendruck-Engine in das Dokument einfügen muss. |
| [getTableName()](#getTableName) | Liefert den Namen der Datentabelle für die aktuelle Zusammenführungsoperation oder einen leeren String, wenn der Name nicht verfügbar ist. |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object) | Setzt den Wert des Feldes aus der Datenquelle. |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage) | Gibt das Bild an, das die Seriendruck‑Engine in das Dokument einfügen muss. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Legt den Dateinamen des Bildes fest, das die Seriendruck‑Engine in das Dokument einfügen muss. |
| [setImageHeight(MergeFieldImageDimension value)](#setImageHeight-com.aspose.words.MergeFieldImageDimension) | Gibt die Bildhöhe für das in das Dokument einzufügende Bild an. |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream) |  |
| [setImageWidth(MergeFieldImageDimension value)](#setImageWidth-com.aspose.words.MergeFieldImageDimension) | Gibt die Bildbreite für das in das Dokument einzufügende Bild an. |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape) | Gibt die Form an, die die Seriendruck-Engine in das Dokument einfügen muss. |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Gibt das [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument)-Objekt zurück, für das der Seriendruck ausgeführt wird.

 **Examples:** 

Zeigt, wie ein Seriendruck mit einem benutzerdefinierten Callback ausgeführt wird, der Zusammenführungsdaten in Form von HTML‑Dokumenten verarbeitet.

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


Liefert den Namen des Seriendruckfeldes, wie im Dokument angegeben.

 **Remarks:** 

Wenn Sie eine Zuordnung von einem Dokumentfeldnamen zu einem anderen Datenquellenfeldnamen haben, ist dies der ursprüngliche Feldname, wie im Dokument angegeben.

Wenn Sie einen Feldnamenpräfix angegeben haben, zum Beispiel "Image:MyFieldName" im Dokument, dann gibt [getDocumentFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getDocumentFieldName) den Feldnamen ohne Präfix zurück, also "MyFieldName".

 **Examples:** 

Zeigt, wie ein Seriendruck mit einem benutzerdefinierten Callback ausgeführt wird, der Zusammenführungsdaten in Form von HTML‑Dokumenten verarbeitet.

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
java.lang.String - Der Name des Seriendruckfeldes, wie im Dokument angegeben.
### getField() {#getField}
```
public FieldMergeField getField()
```


Liefert das Objekt, das das aktuelle Seriendruckfeld repräsentiert.

 **Examples:** 

Zeigt, wie ein Seriendruck mit einem benutzerdefinierten Callback ausgeführt wird, der Zusammenführungsdaten in Form von HTML‑Dokumenten verarbeitet.

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


Liefert den Namen des Seriendruckfeldes in der Datenquelle.

 **Remarks:** 

Wenn Sie eine Zuordnung von einem Dokumentfeldnamen zu einem anderen Datenquellenfeldnamen haben, ist dies der zugeordnete Feldname.

Wenn Sie einen Feldnamenpräfix angegeben haben, zum Beispiel "Image:MyFieldName" im Dokument, dann gibt [getFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getFieldName) den Feldnamen ohne Präfix zurück, also "MyFieldName".

 **Examples:** 

Zeigt, wie Checkbox-Formularfelder während eines Seriendrucks in ein Dokument eingefügt werden.

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
java.lang.String - Der Name des Seriendruckfeldes in der Datenquelle.
### getFieldValue() {#getFieldValue}
```
public Object getFieldValue()
```


Liefert den Wert des Feldes aus der Datenquelle.

 **Remarks:** 

Diese Eigenschaft enthält einen Wert, der gerade von Ihrer Datenquelle für dieses Feld durch die Seriendruck-Engine ausgewählt wurde. Sie können den Wert auch ersetzen, indem Sie die Eigenschaft setzen.

 **Examples:** 

Zeigt, wie der Datenquellenwert des Feldes verwendet wird.

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
java.lang.Object - Der Wert des Feldes aus der Datenquelle.
### getImage() {#getImage}
```
public BufferedImage getImage()
```


Gibt das Bild an, das die Seriendruck‑Engine in das Dokument einfügen muss.

 **Examples:** 

Zeigt, wie ein Callback verwendet wird, um die Logik des Bildzusammenführens anzupassen.

```

 public void mergeFieldImages() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source which contains local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // In this case, the field expects the data source to have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Filenames can be lengthy, and if we can find a way to avoid storing them in the data source,
     // we may considerably reduce its size.
     // Create a data source that refers to images using short names.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add("Dark logo");
     dataTable.getRows().add("Transparent logo");

     // Assign a merging callback that contains all logic that processes those names,
     // and then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new ImageFilenameCallback());
     doc.getMailMerge().execute(dataTable);

     doc.save(getArtifactsDir() + "Field.MERGEFIELD.Images.docx");
 }

 /// 
 /// Contains a dictionary that maps names of images to local system filenames that contain these images.
 /// If a mail merge data source uses one of the dictionary's names to refer to an image,
 /// this callback will pass the respective filename to the merge destination.
 /// 
 private static class ImageFilenameCallback implements IFieldMergingCallback {
     public ImageFilenameCallback() {
         mImageFilenames.put("Dark logo", getImageDir() + "Logo.jpg");
         mImageFilenames.put("Transparent logo", getImageDir() + "Transparent background logo.png");
     }

     public void fieldMerging(FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) throws IOException {
         if (mImageFilenames.containsKey(args.getFieldValue().toString())) {
             args.setImage(ImageIO.read(new File(mImageFilenames.get(args.getFieldValue().toString()))));
         }

         Assert.assertNotNull(args.getImage());
     }

     private final HashMap mImageFilenames = new HashMap<>();
 }
 
```

**Returns:**
java.awt.image.BufferedImage – Der entsprechende java.awt.image.BufferedImage‑Wert.
### getImageFileName() {#getImageFileName}
```
public String getImageFileName()
```


Legt den Dateinamen des Bildes fest, das die Seriendruck‑Engine in das Dokument einfügen muss.

 **Examples:** 

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wie MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```

 public void mergeFieldImageDimension() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source containing local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // The data source should have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Create a suitable data source.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add(getImageDir() + "Logo.jpg");
     dataTable.getRows().add(getImageDir() + "Transparent background logo.png");
     dataTable.getRows().add(getImageDir() + "Enhanced Windows MetaFile.emf");

     // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new MergedImageResizer(200.0, 200.0, MergeFieldImageDimensionUnit.POINT));
     doc.getMailMerge().execute(dataTable);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.MERGEFIELD.ImageDimension.docx");
 }

 /// 
 /// Sets the size of all mail merged images to one defined width and height.
 /// 
 private static class MergedImageResizer implements IFieldMergingCallback {
     public MergedImageResizer(final double imageWidth, final double imageHeight, final int unit) {
         mImageWidth = imageWidth;
         mImageHeight = imageHeight;
         mUnit = unit;
     }

     public void fieldMerging(final FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         args.setImageFileName(args.getFieldValue().toString());
         args.setImageWidth(new MergeFieldImageDimension(mImageWidth, mUnit));
         args.setImageHeight(new MergeFieldImageDimension(mImageHeight, mUnit));

         Assert.assertEquals(mImageWidth, args.getImageWidth().getValue());
         Assert.assertEquals(mUnit, args.getImageWidth().getUnit());
         Assert.assertEquals(mImageHeight, args.getImageHeight().getValue());
         Assert.assertEquals(mUnit, args.getImageHeight().getUnit());
         Assert.assertNull(args.getShape());
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Returns:**
java.lang.String – Der Dateiname des Bildes, das die Seriendruck-Engine in das Dokument einfügen muss.
### getImageHeight() {#getImageHeight}
```
public MergeFieldImageDimension getImageHeight()
```


Gibt die Bildhöhe für das in das Dokument einzufügende Bild an.

 **Remarks:** 

Der Wert dieser Eigenschaft stammt zunächst aus dem entsprechenden MERGEFIELD‑Code, der im Vorlagendokument enthalten ist. Um den Anfangswert zu überschreiben, sollten Sie dieser Eigenschaft eine Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) zuweisen oder die Eigenschaften der von dieser Eigenschaft zurückgegebenen Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) festlegen.

Um anzuzeigen, dass der ursprüngliche Wert der Bildhöhe verwendet werden soll, sollten Sie dieser Eigenschaft den  null  Wert zuweisen oder die [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) Eigenschaft für die von dieser Eigenschaft zurückgegebene Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) auf einen negativen Wert setzen.

 **Examples:** 

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wie MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```

 public void mergeFieldImageDimension() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source containing local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // The data source should have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Create a suitable data source.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add(getImageDir() + "Logo.jpg");
     dataTable.getRows().add(getImageDir() + "Transparent background logo.png");
     dataTable.getRows().add(getImageDir() + "Enhanced Windows MetaFile.emf");

     // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new MergedImageResizer(200.0, 200.0, MergeFieldImageDimensionUnit.POINT));
     doc.getMailMerge().execute(dataTable);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.MERGEFIELD.ImageDimension.docx");
 }

 /// 
 /// Sets the size of all mail merged images to one defined width and height.
 /// 
 private static class MergedImageResizer implements IFieldMergingCallback {
     public MergedImageResizer(final double imageWidth, final double imageHeight, final int unit) {
         mImageWidth = imageWidth;
         mImageHeight = imageHeight;
         mUnit = unit;
     }

     public void fieldMerging(final FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         args.setImageFileName(args.getFieldValue().toString());
         args.setImageWidth(new MergeFieldImageDimension(mImageWidth, mUnit));
         args.setImageHeight(new MergeFieldImageDimension(mImageHeight, mUnit));

         Assert.assertEquals(mImageWidth, args.getImageWidth().getValue());
         Assert.assertEquals(mUnit, args.getImageWidth().getUnit());
         Assert.assertEquals(mImageHeight, args.getImageHeight().getValue());
         Assert.assertEquals(mUnit, args.getImageHeight().getUnit());
         Assert.assertNull(args.getShape());
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Returns:**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) - The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) value.
### getImageStream() {#getImageStream}
```
public InputStream getImageStream()
```




**Returns:**
java.io.InputStream
### getImageWidth() {#getImageWidth}
```
public MergeFieldImageDimension getImageWidth()
```


Gibt die Bildbreite für das in das Dokument einzufügende Bild an.

 **Remarks:** 

Der Wert dieser Eigenschaft stammt zunächst aus dem entsprechenden MERGEFIELD‑Code, der im Vorlagendokument enthalten ist. Um den Anfangswert zu überschreiben, sollten Sie dieser Eigenschaft eine Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) zuweisen oder die Eigenschaften der von dieser Eigenschaft zurückgegebenen Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) festlegen.

Um anzuzeigen, dass der ursprüngliche Wert der Bildbreite verwendet werden soll, sollten Sie dieser Eigenschaft den  null  Wert zuweisen oder die [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) Eigenschaft für die von dieser Eigenschaft zurückgegebene Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) auf einen negativen Wert setzen.

 **Examples:** 

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wie MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```

 public void mergeFieldImageDimension() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source containing local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // The data source should have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Create a suitable data source.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add(getImageDir() + "Logo.jpg");
     dataTable.getRows().add(getImageDir() + "Transparent background logo.png");
     dataTable.getRows().add(getImageDir() + "Enhanced Windows MetaFile.emf");

     // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new MergedImageResizer(200.0, 200.0, MergeFieldImageDimensionUnit.POINT));
     doc.getMailMerge().execute(dataTable);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.MERGEFIELD.ImageDimension.docx");
 }

 /// 
 /// Sets the size of all mail merged images to one defined width and height.
 /// 
 private static class MergedImageResizer implements IFieldMergingCallback {
     public MergedImageResizer(final double imageWidth, final double imageHeight, final int unit) {
         mImageWidth = imageWidth;
         mImageHeight = imageHeight;
         mUnit = unit;
     }

     public void fieldMerging(final FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         args.setImageFileName(args.getFieldValue().toString());
         args.setImageWidth(new MergeFieldImageDimension(mImageWidth, mUnit));
         args.setImageHeight(new MergeFieldImageDimension(mImageHeight, mUnit));

         Assert.assertEquals(mImageWidth, args.getImageWidth().getValue());
         Assert.assertEquals(mUnit, args.getImageWidth().getUnit());
         Assert.assertEquals(mImageHeight, args.getImageHeight().getValue());
         Assert.assertEquals(mUnit, args.getImageHeight().getUnit());
         Assert.assertNull(args.getShape());
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Returns:**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) - The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) value.
### getRecordIndex() {#getRecordIndex}
```
public int getRecordIndex()
```


Liefert den nullbasierten Index des Datensatzes, der zusammengeführt wird.

 **Examples:** 

Zeigt, wie Checkbox-Formularfelder während eines Seriendrucks in ein Dokument eingefügt werden.

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
int - Der nullbasierte Index des Datensatzes, der zusammengeführt wird.
### getShape() {#getShape}
```
public Shape getShape()
```


Gibt die Form an, die die Seriendruck-Engine in das Dokument einfügen muss.

 **Remarks:** 

Wenn diese Eigenschaft angegeben ist, ignoriert die Seriendruck-Engine alle anderen Eigenschaften wie [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) oder **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** und fügt einfach die Form in das Dokument ein.

Verwenden Sie diese Eigenschaft, um den Vorgang des Zusammenführens eines Bild-Seriendruckfelds vollständig zu steuern. Beispielsweise können Sie [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) oder eine andere Formeigenschaft angeben, um den resultierenden Knoten fein abzustimmen. Bitte beachten Sie jedoch, dass Sie für die Bereitstellung des Inhalts der Form verantwortlich sind.

 **Examples:** 

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wie MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```

 public void mergeFieldImageDimension() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source containing local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // The data source should have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Create a suitable data source.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add(getImageDir() + "Logo.jpg");
     dataTable.getRows().add(getImageDir() + "Transparent background logo.png");
     dataTable.getRows().add(getImageDir() + "Enhanced Windows MetaFile.emf");

     // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new MergedImageResizer(200.0, 200.0, MergeFieldImageDimensionUnit.POINT));
     doc.getMailMerge().execute(dataTable);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.MERGEFIELD.ImageDimension.docx");
 }

 /// 
 /// Sets the size of all mail merged images to one defined width and height.
 /// 
 private static class MergedImageResizer implements IFieldMergingCallback {
     public MergedImageResizer(final double imageWidth, final double imageHeight, final int unit) {
         mImageWidth = imageWidth;
         mImageHeight = imageHeight;
         mUnit = unit;
     }

     public void fieldMerging(final FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         args.setImageFileName(args.getFieldValue().toString());
         args.setImageWidth(new MergeFieldImageDimension(mImageWidth, mUnit));
         args.setImageHeight(new MergeFieldImageDimension(mImageHeight, mUnit));

         Assert.assertEquals(mImageWidth, args.getImageWidth().getValue());
         Assert.assertEquals(mUnit, args.getImageWidth().getUnit());
         Assert.assertEquals(mImageHeight, args.getImageHeight().getValue());
         Assert.assertEquals(mUnit, args.getImageHeight().getUnit());
         Assert.assertNull(args.getShape());
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Returns:**
[Shape](../../com.aspose.words/shape/) - The corresponding [Shape](../../com.aspose.words/shape/) value.
### getTableName() {#getTableName}
```
public String getTableName()
```


Liefert den Namen der Datentabelle für die aktuelle Zusammenführungsoperation oder einen leeren String, wenn der Name nicht verfügbar ist.

 **Examples:** 

Zeigt, wie Checkbox-Formularfelder während eines Seriendrucks in ein Dokument eingefügt werden.

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
java.lang.String - Der Name der Datentabelle für die aktuelle Zusammenführungsoperation oder ein leerer String, wenn der Name nicht verfügbar ist.
### setFieldValue(Object value) {#setFieldValue-java.lang.Object}
```
public void setFieldValue(Object value)
```


Setzt den Wert des Feldes aus der Datenquelle.

 **Remarks:** 

Diese Eigenschaft enthält einen Wert, der gerade von Ihrer Datenquelle für dieses Feld durch die Seriendruck-Engine ausgewählt wurde. Sie können den Wert auch ersetzen, indem Sie die Eigenschaft setzen.

 **Examples:** 

Zeigt, wie der Datenquellenwert des Feldes verwendet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.Object | Der Wert des Feldes aus der Datenquelle. |

### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage value)
```


Gibt das Bild an, das die Seriendruck‑Engine in das Dokument einfügen muss.

 **Examples:** 

Zeigt, wie ein Callback verwendet wird, um die Logik des Bildzusammenführens anzupassen.

```

 public void mergeFieldImages() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source which contains local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // In this case, the field expects the data source to have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Filenames can be lengthy, and if we can find a way to avoid storing them in the data source,
     // we may considerably reduce its size.
     // Create a data source that refers to images using short names.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add("Dark logo");
     dataTable.getRows().add("Transparent logo");

     // Assign a merging callback that contains all logic that processes those names,
     // and then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new ImageFilenameCallback());
     doc.getMailMerge().execute(dataTable);

     doc.save(getArtifactsDir() + "Field.MERGEFIELD.Images.docx");
 }

 /// 
 /// Contains a dictionary that maps names of images to local system filenames that contain these images.
 /// If a mail merge data source uses one of the dictionary's names to refer to an image,
 /// this callback will pass the respective filename to the merge destination.
 /// 
 private static class ImageFilenameCallback implements IFieldMergingCallback {
     public ImageFilenameCallback() {
         mImageFilenames.put("Dark logo", getImageDir() + "Logo.jpg");
         mImageFilenames.put("Transparent logo", getImageDir() + "Transparent background logo.png");
     }

     public void fieldMerging(FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) throws IOException {
         if (mImageFilenames.containsKey(args.getFieldValue().toString())) {
             args.setImage(ImageIO.read(new File(mImageFilenames.get(args.getFieldValue().toString()))));
         }

         Assert.assertNotNull(args.getImage());
     }

     private final HashMap mImageFilenames = new HashMap<>();
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.image.BufferedImage | Der entsprechende java.awt.image.BufferedImage‑Wert. |

### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Legt den Dateinamen des Bildes fest, das die Seriendruck‑Engine in das Dokument einfügen muss.

 **Examples:** 

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wie MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```

 public void mergeFieldImageDimension() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source containing local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // The data source should have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Create a suitable data source.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add(getImageDir() + "Logo.jpg");
     dataTable.getRows().add(getImageDir() + "Transparent background logo.png");
     dataTable.getRows().add(getImageDir() + "Enhanced Windows MetaFile.emf");

     // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new MergedImageResizer(200.0, 200.0, MergeFieldImageDimensionUnit.POINT));
     doc.getMailMerge().execute(dataTable);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.MERGEFIELD.ImageDimension.docx");
 }

 /// 
 /// Sets the size of all mail merged images to one defined width and height.
 /// 
 private static class MergedImageResizer implements IFieldMergingCallback {
     public MergedImageResizer(final double imageWidth, final double imageHeight, final int unit) {
         mImageWidth = imageWidth;
         mImageHeight = imageHeight;
         mUnit = unit;
     }

     public void fieldMerging(final FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         args.setImageFileName(args.getFieldValue().toString());
         args.setImageWidth(new MergeFieldImageDimension(mImageWidth, mUnit));
         args.setImageHeight(new MergeFieldImageDimension(mImageHeight, mUnit));

         Assert.assertEquals(mImageWidth, args.getImageWidth().getValue());
         Assert.assertEquals(mUnit, args.getImageWidth().getUnit());
         Assert.assertEquals(mImageHeight, args.getImageHeight().getValue());
         Assert.assertEquals(mUnit, args.getImageHeight().getUnit());
         Assert.assertNull(args.getShape());
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Dateiname des Bildes, das die Seriendruck-Engine in das Dokument einfügen muss. |

### setImageHeight(MergeFieldImageDimension value) {#setImageHeight-com.aspose.words.MergeFieldImageDimension}
```
public void setImageHeight(MergeFieldImageDimension value)
```


Gibt die Bildhöhe für das in das Dokument einzufügende Bild an.

 **Remarks:** 

Der Wert dieser Eigenschaft stammt zunächst aus dem entsprechenden MERGEFIELD‑Code, der im Vorlagendokument enthalten ist. Um den Anfangswert zu überschreiben, sollten Sie dieser Eigenschaft eine Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) zuweisen oder die Eigenschaften der von dieser Eigenschaft zurückgegebenen Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) festlegen.

Um anzuzeigen, dass der ursprüngliche Wert der Bildhöhe verwendet werden soll, sollten Sie dieser Eigenschaft den  null  Wert zuweisen oder die [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) Eigenschaft für die von dieser Eigenschaft zurückgegebene Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) auf einen negativen Wert setzen.

 **Examples:** 

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wie MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```

 public void mergeFieldImageDimension() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source containing local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // The data source should have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Create a suitable data source.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add(getImageDir() + "Logo.jpg");
     dataTable.getRows().add(getImageDir() + "Transparent background logo.png");
     dataTable.getRows().add(getImageDir() + "Enhanced Windows MetaFile.emf");

     // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new MergedImageResizer(200.0, 200.0, MergeFieldImageDimensionUnit.POINT));
     doc.getMailMerge().execute(dataTable);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.MERGEFIELD.ImageDimension.docx");
 }

 /// 
 /// Sets the size of all mail merged images to one defined width and height.
 /// 
 private static class MergedImageResizer implements IFieldMergingCallback {
     public MergedImageResizer(final double imageWidth, final double imageHeight, final int unit) {
         mImageWidth = imageWidth;
         mImageHeight = imageHeight;
         mUnit = unit;
     }

     public void fieldMerging(final FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         args.setImageFileName(args.getFieldValue().toString());
         args.setImageWidth(new MergeFieldImageDimension(mImageWidth, mUnit));
         args.setImageHeight(new MergeFieldImageDimension(mImageHeight, mUnit));

         Assert.assertEquals(mImageWidth, args.getImageWidth().getValue());
         Assert.assertEquals(mUnit, args.getImageWidth().getUnit());
         Assert.assertEquals(mImageHeight, args.getImageHeight().getValue());
         Assert.assertEquals(mUnit, args.getImageHeight().getUnit());
         Assert.assertNull(args.getShape());
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | Der entsprechende [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) Wert. |

### setImageStream(InputStream value) {#setImageStream-java.io.InputStream}
```
public void setImageStream(InputStream value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.io.InputStream |  |

### setImageWidth(MergeFieldImageDimension value) {#setImageWidth-com.aspose.words.MergeFieldImageDimension}
```
public void setImageWidth(MergeFieldImageDimension value)
```


Gibt die Bildbreite für das in das Dokument einzufügende Bild an.

 **Remarks:** 

Der Wert dieser Eigenschaft stammt zunächst aus dem entsprechenden MERGEFIELD‑Code, der im Vorlagendokument enthalten ist. Um den Anfangswert zu überschreiben, sollten Sie dieser Eigenschaft eine Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) zuweisen oder die Eigenschaften der von dieser Eigenschaft zurückgegebenen Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) festlegen.

Um anzuzeigen, dass der ursprüngliche Wert der Bildbreite verwendet werden soll, sollten Sie dieser Eigenschaft den  null  Wert zuweisen oder die [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) Eigenschaft für die von dieser Eigenschaft zurückgegebene Instanz der Klasse [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) auf einen negativen Wert setzen.

 **Examples:** 

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wie MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```

 public void mergeFieldImageDimension() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source containing local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // The data source should have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Create a suitable data source.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add(getImageDir() + "Logo.jpg");
     dataTable.getRows().add(getImageDir() + "Transparent background logo.png");
     dataTable.getRows().add(getImageDir() + "Enhanced Windows MetaFile.emf");

     // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new MergedImageResizer(200.0, 200.0, MergeFieldImageDimensionUnit.POINT));
     doc.getMailMerge().execute(dataTable);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.MERGEFIELD.ImageDimension.docx");
 }

 /// 
 /// Sets the size of all mail merged images to one defined width and height.
 /// 
 private static class MergedImageResizer implements IFieldMergingCallback {
     public MergedImageResizer(final double imageWidth, final double imageHeight, final int unit) {
         mImageWidth = imageWidth;
         mImageHeight = imageHeight;
         mUnit = unit;
     }

     public void fieldMerging(final FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         args.setImageFileName(args.getFieldValue().toString());
         args.setImageWidth(new MergeFieldImageDimension(mImageWidth, mUnit));
         args.setImageHeight(new MergeFieldImageDimension(mImageHeight, mUnit));

         Assert.assertEquals(mImageWidth, args.getImageWidth().getValue());
         Assert.assertEquals(mUnit, args.getImageWidth().getUnit());
         Assert.assertEquals(mImageHeight, args.getImageHeight().getValue());
         Assert.assertEquals(mUnit, args.getImageHeight().getUnit());
         Assert.assertNull(args.getShape());
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | Der entsprechende [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) Wert. |

### setShape(Shape value) {#setShape-com.aspose.words.Shape}
```
public void setShape(Shape value)
```


Gibt die Form an, die die Seriendruck-Engine in das Dokument einfügen muss.

 **Remarks:** 

Wenn diese Eigenschaft angegeben ist, ignoriert die Seriendruck-Engine alle anderen Eigenschaften wie [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) oder **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** und fügt einfach die Form in das Dokument ein.

Verwenden Sie diese Eigenschaft, um den Vorgang des Zusammenführens eines Bild-Seriendruckfelds vollständig zu steuern. Beispielsweise können Sie [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) oder eine andere Formeigenschaft angeben, um den resultierenden Knoten fein abzustimmen. Bitte beachten Sie jedoch, dass Sie für die Bereitstellung des Inhalts der Form verantwortlich sind.

 **Examples:** 

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wie MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```

 public void mergeFieldImageDimension() throws Exception {
     Document doc = new Document();

     // Insert a MERGEFIELD that will accept images from a source during a mail merge. Use the field code to reference
     // a column in the data source containing local system filenames of images we wish to use in the mail merge.
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldMergeField field = (FieldMergeField) builder.insertField("MERGEFIELD Image:ImageColumn");

     // The data source should have such a column named "ImageColumn".
     Assert.assertEquals("Image:ImageColumn", field.getFieldName());

     // Create a suitable data source.
     DataTable dataTable = new DataTable("Images");
     dataTable.getColumns().add(new DataColumn("ImageColumn"));
     dataTable.getRows().add(getImageDir() + "Logo.jpg");
     dataTable.getRows().add(getImageDir() + "Transparent background logo.png");
     dataTable.getRows().add(getImageDir() + "Enhanced Windows MetaFile.emf");

     // Configure a callback to modify the sizes of images at merge time, then execute the mail merge.
     doc.getMailMerge().setFieldMergingCallback(new MergedImageResizer(200.0, 200.0, MergeFieldImageDimensionUnit.POINT));
     doc.getMailMerge().execute(dataTable);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.MERGEFIELD.ImageDimension.docx");
 }

 /// 
 /// Sets the size of all mail merged images to one defined width and height.
 /// 
 private static class MergedImageResizer implements IFieldMergingCallback {
     public MergedImageResizer(final double imageWidth, final double imageHeight, final int unit) {
         mImageWidth = imageWidth;
         mImageHeight = imageHeight;
         mUnit = unit;
     }

     public void fieldMerging(final FieldMergingArgs args) {
         throw new UnsupportedOperationException();
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         args.setImageFileName(args.getFieldValue().toString());
         args.setImageWidth(new MergeFieldImageDimension(mImageWidth, mUnit));
         args.setImageHeight(new MergeFieldImageDimension(mImageHeight, mUnit));

         Assert.assertEquals(mImageWidth, args.getImageWidth().getValue());
         Assert.assertEquals(mUnit, args.getImageWidth().getUnit());
         Assert.assertEquals(mImageHeight, args.getImageHeight().getValue());
         Assert.assertEquals(mUnit, args.getImageHeight().getUnit());
         Assert.assertNull(args.getShape());
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape/) | Der entsprechende [Shape](../../com.aspose.words/shape/) Wert. |

