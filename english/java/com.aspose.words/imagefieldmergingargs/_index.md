---
title: ImageFieldMergingArgs
linktitle: ImageFieldMergingArgs
second_title: Aspose.Words for Java
description: Provides data for the IFieldMergingCallback.imageFieldMergingcom.aspose.words.ImageFieldMergingArgs event in Java.
type: docs
weight: 368
url: /java/com.aspose.words/imagefieldmergingargs/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase/)
```
public class ImageFieldMergingArgs extends FieldMergingArgsBase
```

Provides data for the [IFieldMergingCallback.imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../../com.aspose.words/ifieldmergingcallback/\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs) event.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

 **Remarks:** 

This event occurs during mail merge when an image mail merge field is encountered in the document. You can respond to this event to return a file name, stream, or an java.awt.image.BufferedImage object to the mail merge engine so it is inserted into the document.

There are three properties available [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String), **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** and [getImage()](../../com.aspose.words/imagefieldmergingargs/\#getImage) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs/\#setImage-java.awt.image.BufferedImage) to specify where the image must be taken from. Set only one of these properties.

To insert an image mail merge field into a document in Word, select Insert/Field command, then select MergeField and type Image:MyFieldName.

 **Examples:** 

Shows how to insert images stored in a database BLOB field into a report.

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

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge.

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
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methods

| Method | Description |
| --- | --- |
| [getDocument()](#getDocument) | Returns the [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) object for which the mail merge is performed. |
| [getDocumentFieldName()](#getDocumentFieldName) | Gets the name of the merge field as specified in the document. |
| [getField()](#getField) | Gets the object that represents the current merge field. |
| [getFieldName()](#getFieldName) | Gets the name of the merge field in the data source. |
| [getFieldValue()](#getFieldValue) | Gets the value of the field from the data source. |
| [getImage()](#getImage) | Specifies the image that the mail merge engine must insert into the document. |
| [getImageFileName()](#getImageFileName) | Sets the file name of the image that the mail merge engine must insert into the document. |
| [getImageHeight()](#getImageHeight) | Specifies the image height for the image to insert into the document. |
| [getImageStream()](#getImageStream) |  |
| [getImageWidth()](#getImageWidth) | Specifies the image width for the image to insert into the document. |
| [getRecordIndex()](#getRecordIndex) | Gets the zero based index of the record that is being merged. |
| [getShape()](#getShape) | Specifies the shape that the mail merge engine must insert into the document. |
| [getTableName()](#getTableName) | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object) | Sets the value of the field from the data source. |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage) | Specifies the image that the mail merge engine must insert into the document. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Sets the file name of the image that the mail merge engine must insert into the document. |
| [setImageHeight(MergeFieldImageDimension value)](#setImageHeight-com.aspose.words.MergeFieldImageDimension) | Specifies the image height for the image to insert into the document. |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream) |  |
| [setImageWidth(MergeFieldImageDimension value)](#setImageWidth-com.aspose.words.MergeFieldImageDimension) | Specifies the image width for the image to insert into the document. |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape) | Specifies the shape that the mail merge engine must insert into the document. |
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
### getImage() {#getImage}
```
public BufferedImage getImage()
```


Specifies the image that the mail merge engine must insert into the document.

 **Examples:** 

Shows how to use a callback to customize image merging logic.

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
java.awt.image.BufferedImage - The corresponding java.awt.image.BufferedImage value.
### getImageFileName() {#getImageFileName}
```
public String getImageFileName()
```


Sets the file name of the image that the mail merge engine must insert into the document.

 **Examples:** 

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge.

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
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Returns:**
java.lang.String - The file name of the image that the mail merge engine must insert into the document.
### getImageHeight() {#getImageHeight}
```
public MergeFieldImageDimension getImageHeight()
```


Specifies the image height for the image to insert into the document.

 **Remarks:** 

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class, returned by this property.

To indicate that the original value of the image height should be applied, you should assign the  null  value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class, returned by this property, to a negative value.

 **Examples:** 

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge.

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


Specifies the image width for the image to insert into the document.

 **Remarks:** 

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class, returned by this property.

To indicate that the original value of the image width should be applied, you should assign the  null  value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class, returned by this property, to a negative value.

 **Examples:** 

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge.

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
### getShape() {#getShape}
```
public Shape getShape()
```


Specifies the shape that the mail merge engine must insert into the document.

 **Remarks:** 

When this property is specified, the mail merge engine ignores all other properties like [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) or **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field. For example, you can specify [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) or any other shape property to fine tune the resulting node. However, please note that you are responsible for providing the content of the shape.

**Returns:**
[Shape](../../com.aspose.words/shape/) - The corresponding [Shape](../../com.aspose.words/shape/) value.
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

### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage value)
```


Specifies the image that the mail merge engine must insert into the document.

 **Examples:** 

Shows how to use a callback to customize image merging logic.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.image.BufferedImage | The corresponding java.awt.image.BufferedImage value. |

### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Sets the file name of the image that the mail merge engine must insert into the document.

 **Examples:** 

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge.

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
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name of the image that the mail merge engine must insert into the document. |

### setImageHeight(MergeFieldImageDimension value) {#setImageHeight-com.aspose.words.MergeFieldImageDimension}
```
public void setImageHeight(MergeFieldImageDimension value)
```


Specifies the image height for the image to insert into the document.

 **Remarks:** 

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class, returned by this property.

To indicate that the original value of the image height should be applied, you should assign the  null  value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class, returned by this property, to a negative value.

 **Examples:** 

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge.

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
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) value. |

### setImageStream(InputStream value) {#setImageStream-java.io.InputStream}
```
public void setImageStream(InputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.InputStream |  |

### setImageWidth(MergeFieldImageDimension value) {#setImageWidth-com.aspose.words.MergeFieldImageDimension}
```
public void setImageWidth(MergeFieldImageDimension value)
```


Specifies the image width for the image to insert into the document.

 **Remarks:** 

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class, returned by this property.

To indicate that the original value of the image width should be applied, you should assign the  null  value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) class, returned by this property, to a negative value.

 **Examples:** 

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge.

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
     }

     private final double mImageWidth;
     private final double mImageHeight;
     private final int mUnit;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) value. |

### setShape(Shape value) {#setShape-com.aspose.words.Shape}
```
public void setShape(Shape value)
```


Specifies the shape that the mail merge engine must insert into the document.

 **Remarks:** 

When this property is specified, the mail merge engine ignores all other properties like [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) or **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field. For example, you can specify [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) or any other shape property to fine tune the resulting node. However, please note that you are responsible for providing the content of the shape.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape/) | The corresponding [Shape](../../com.aspose.words/shape/) value. |

