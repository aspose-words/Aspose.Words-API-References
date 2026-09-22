---
title: "ImageFieldMergingArgs"
linktitle: "ImageFieldMergingArgs"
second_title: "Aspose.Words لـ Java"
description: "يوفر البيانات لحدث IFieldMergingCallback.imageFieldMergingcom.aspose.words.ImageFieldMergingArgs في Java."
type: docs
weight: 392
url: /ar/java/com.aspose.words/imagefieldmergingargs/
---

**Inheritance:**
java.lang.Object، [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase/)
```
public class ImageFieldMergingArgs extends FieldMergingArgsBase
```

يوفر البيانات لحدث [IFieldMergingCallback.imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../../com.aspose.words/ifieldmergingcallback/\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs).

لمزيد من المعلومات، قم بزيارة [ Mail Merge and Reporting ][Mail Merge and Reporting] مقالة التوثيق.

 **Remarks:** 

يحدث هذا الحدث أثناء دمج البريد عندما يتم العثور على حقل دمج صورة في المستند. يمكنك الاستجابة لهذا الحدث لإرجاع اسم ملف أو تدفق أو كائن java.awt.image.BufferedImage إلى محرك دمج البريد ليتم إدراجه في المستند.

هناك ثلاث خصائص متاحة [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String)، **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** و [getImage()](../../com.aspose.words/imagefieldmergingargs/\#getImage) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs/\#setImage-java.awt.image.BufferedImage) لتحديد مصدر الصورة. قم بتعيين واحدة فقط من هذه الخصائص.

لإدراج حقل دمج صورة في مستند Word، اختر أمر Insert/Field، ثم حدد MergeField واكتب Image:MyFieldName.

 **Examples:** 

يوضح كيفية ضبط أبعاد الصور كما تقبلها MERGEFIELDS أثناء دمج البريد.

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

يوضح كيفية إدراج الصور المخزنة في حقل BLOB بقاعدة البيانات في تقرير.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getDocument()](#getDocument) | يعيد كائن [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) الذي يتم تنفيذ دمج البريد عليه. |
| [getDocumentFieldName()](#getDocumentFieldName) | يحصل على اسم حقل الدمج كما هو محدد في المستند. |
| [getField()](#getField) | يحصل على الكائن الذي يمثل حقل الدمج الحالي. |
| [getFieldName()](#getFieldName) | يحصل على اسم حقل الدمج في مصدر البيانات. |
| [getFieldValue()](#getFieldValue) | يحصل على قيمة الحقل من مصدر البيانات. |
| [getImage()](#getImage) | يحدد الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [getImageFileName()](#getImageFileName) | يضبط اسم ملف الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [getImageHeight()](#getImageHeight) | يحدد ارتفاع الصورة لإدراجها في المستند. |
| [getImageStream()](#getImageStream) |  |
| [getImageWidth()](#getImageWidth) | يحدد عرض الصورة لإدراجها في المستند. |
| [getRecordIndex()](#getRecordIndex) | يحصل على الفهرس الصفري للسجل الذي يتم دمجه. |
| [getShape()](#getShape) | يحدد الشكل الذي يجب على محرك دمج البريد إدراجه في المستند. |
| [getTableName()](#getTableName) | يحصل على اسم جدول البيانات لعملية الدمج الحالية أو سلسلة فارغة إذا لم يتوفر الاسم. |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object) | يضبط قيمة الحقل من مصدر البيانات. |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage) | يحدد الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | يضبط اسم ملف الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [setImageHeight(MergeFieldImageDimension value)](#setImageHeight-com.aspose.words.MergeFieldImageDimension) | يحدد ارتفاع الصورة لإدراجها في المستند. |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream) |  |
| [setImageWidth(MergeFieldImageDimension value)](#setImageWidth-com.aspose.words.MergeFieldImageDimension) | يحدد عرض الصورة لإدراجها في المستند. |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape) | يحدد الشكل الذي يجب على محرك دمج البريد إدراجه في المستند. |
### getDocument() {#getDocument}
```
public Document getDocument()
```


يعيد كائن [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) الذي يتم تنفيذ دمج البريد عليه.

 **Examples:** 

يوضح كيفية تنفيذ دمج بريد مع رد اتصال مخصص يتعامل مع بيانات الدمج على شكل مستندات HTML.

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


يحصل على اسم حقل الدمج كما هو محدد في المستند.

 **Remarks:** 

إذا كان لديك تعيين من اسم حقل المستند إلى اسم حقل مختلف في مصدر البيانات، فإن هذا هو اسم الحقل الأصلي كما هو محدد في المستند.

إذا حددت بادئة لاسم الحقل، على سبيل المثال \"Image:MyFieldName\" في المستند، فإن [getDocumentFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getDocumentFieldName) تُعيد اسم الحقل بدون البادئة، وهو \"MyFieldName\".

 **Examples:** 

يوضح كيفية تنفيذ دمج بريد مع رد اتصال مخصص يتعامل مع بيانات الدمج على شكل مستندات HTML.

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
java.lang.String - اسم حقل الدمج كما هو محدد في المستند.
### getField() {#getField}
```
public FieldMergeField getField()
```


يحصل على الكائن الذي يمثل حقل الدمج الحالي.

 **Examples:** 

يوضح كيفية تنفيذ دمج بريد مع رد اتصال مخصص يتعامل مع بيانات الدمج على شكل مستندات HTML.

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


يحصل على اسم حقل الدمج في مصدر البيانات.

 **Remarks:** 

إذا كان لديك تعيين من اسم حقل المستند إلى اسم حقل مختلف في مصدر البيانات، فإن هذا هو اسم الحقل المعين.

إذا حددت بادئة لاسم الحقل، على سبيل المثال \"Image:MyFieldName\" في المستند، فإن [getFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getFieldName) تُعيد اسم الحقل بدون البادئة، وهو \"MyFieldName\".

 **Examples:** 

يوضح كيفية إدراج حقول نموذج خانة الاختيار في مستند أثناء دمج البريد.

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
java.lang.String - اسم حقل الدمج في مصدر البيانات.
### getFieldValue() {#getFieldValue}
```
public Object getFieldValue()
```


يحصل على قيمة الحقل من مصدر البيانات.

 **Remarks:** 

تحتوي هذه الخاصية على قيمة تم اختيارها للتو من مصدر البيانات لهذا الحقل بواسطة محرك دمج البريد. يمكنك أيضًا استبدال القيمة عن طريق ضبط الخاصية.

 **Examples:** 

يوضح كيفية استخدام قيمة مصدر البيانات للحقل.

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
java.lang.Object - قيمة الحقل من مصدر البيانات.
### getImage() {#getImage}
```
public BufferedImage getImage()
```


يحدد الصورة التي يجب على محرك دمج البريد إدراجها في المستند.

 **Examples:** 

يوضح كيفية استخدام رد نداء لتخصيص منطق دمج الصور.

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
java.awt.image.BufferedImage - القيمة المقابلة لـ java.awt.image.BufferedImage.
### getImageFileName() {#getImageFileName}
```
public String getImageFileName()
```


يضبط اسم ملف الصورة التي يجب على محرك دمج البريد إدراجها في المستند.

 **Examples:** 

يوضح كيفية ضبط أبعاد الصور كما تقبلها MERGEFIELDS أثناء دمج البريد.

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
java.lang.String - اسم ملف الصورة التي يجب على محرك دمج البريد إدراجها في المستند.
### getImageHeight() {#getImageHeight}
```
public MergeFieldImageDimension getImageHeight()
```


يحدد ارتفاع الصورة لإدراجها في المستند.

 **Remarks:** 

القيمة الأولية لهذه الخاصية تأتي من رمز MERGEFIELD المقابل، الموجود في مستند القالب. لتجاوز القيمة الأولية، يجب عليك تعيين مثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) إلى هذه الخاصية أو ضبط الخصائص للمثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) الذي تُرجع هذه الخاصية.

للإشارة إلى أنه يجب تطبيق القيمة الأصلية لارتفاع الصورة، يجب عليك تعيين القيمة  null  لهذه الخاصية أو ضبط خاصية [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) للمثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) التي تُرجعها هذه الخاصية إلى قيمة سالبة.

 **Examples:** 

يوضح كيفية ضبط أبعاد الصور كما تقبلها MERGEFIELDS أثناء دمج البريد.

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


يحدد عرض الصورة لإدراجها في المستند.

 **Remarks:** 

القيمة الأولية لهذه الخاصية تأتي من رمز MERGEFIELD المقابل، الموجود في مستند القالب. لتجاوز القيمة الأولية، يجب عليك تعيين مثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) إلى هذه الخاصية أو ضبط الخصائص للمثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) الذي تُرجع هذه الخاصية.

للإشارة إلى أنه يجب تطبيق القيمة الأصلية لعرض الصورة، يجب عليك تعيين القيمة  null  لهذه الخاصية أو ضبط خاصية [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) للمثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) التي تُرجعها هذه الخاصية إلى قيمة سالبة.

 **Examples:** 

يوضح كيفية ضبط أبعاد الصور كما تقبلها MERGEFIELDS أثناء دمج البريد.

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


يحصل على الفهرس الصفري للسجل الذي يتم دمجه.

 **Examples:** 

يوضح كيفية إدراج حقول نموذج خانة الاختيار في مستند أثناء دمج البريد.

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
int - الفهرس الذي يبدأ من الصفر للسجل الذي يتم دمجه.
### getShape() {#getShape}
```
public Shape getShape()
```


يحدد الشكل الذي يجب على محرك دمج البريد إدراجه في المستند.

 **Remarks:** 

عند تحديد هذه الخاصية، يتجاهل محرك دمج البريد جميع الخصائص الأخرى مثل [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) أو **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** ويقوم ببساطة بإدراج الشكل في المستند.

استخدم هذه الخاصية للتحكم الكامل في عملية دمج حقل دمج الصورة. على سبيل المثال، يمكنك تحديد [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) أو أي خاصية أخرى للشكل لضبط النود الناتج بدقة. ومع ذلك، يرجى ملاحظة أنك مسؤول عن توفير محتوى الشكل.

 **Examples:** 

يوضح كيفية ضبط أبعاد الصور كما تقبلها MERGEFIELDS أثناء دمج البريد.

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


يحصل على اسم جدول البيانات لعملية الدمج الحالية أو سلسلة فارغة إذا لم يتوفر الاسم.

 **Examples:** 

يوضح كيفية إدراج حقول نموذج خانة الاختيار في مستند أثناء دمج البريد.

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
java.lang.String - اسم جدول البيانات لعملية الدمج الحالية أو سلسلة فارغة إذا لم يتوفر الاسم.
### setFieldValue(Object value) {#setFieldValue-java.lang.Object}
```
public void setFieldValue(Object value)
```


يضبط قيمة الحقل من مصدر البيانات.

 **Remarks:** 

تحتوي هذه الخاصية على قيمة تم اختيارها للتو من مصدر البيانات لهذا الحقل بواسطة محرك دمج البريد. يمكنك أيضًا استبدال القيمة عن طريق ضبط الخاصية.

 **Examples:** 

يوضح كيفية استخدام قيمة مصدر البيانات للحقل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.Object | قيمة الحقل من مصدر البيانات. |

### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage value)
```


يحدد الصورة التي يجب على محرك دمج البريد إدراجها في المستند.

 **Examples:** 

يوضح كيفية استخدام رد نداء لتخصيص منطق دمج الصور.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.image.BufferedImage | القيمة المقابلة لـ java.awt.image.BufferedImage. |

### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


يضبط اسم ملف الصورة التي يجب على محرك دمج البريد إدراجها في المستند.

 **Examples:** 

يوضح كيفية ضبط أبعاد الصور كما تقبلها MERGEFIELDS أثناء دمج البريد.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم ملف الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |

### setImageHeight(MergeFieldImageDimension value) {#setImageHeight-com.aspose.words.MergeFieldImageDimension}
```
public void setImageHeight(MergeFieldImageDimension value)
```


يحدد ارتفاع الصورة لإدراجها في المستند.

 **Remarks:** 

القيمة الأولية لهذه الخاصية تأتي من رمز MERGEFIELD المقابل، الموجود في مستند القالب. لتجاوز القيمة الأولية، يجب عليك تعيين مثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) إلى هذه الخاصية أو ضبط الخصائص للمثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) الذي تُرجع هذه الخاصية.

للإشارة إلى أنه يجب تطبيق القيمة الأصلية لارتفاع الصورة، يجب عليك تعيين القيمة  null  لهذه الخاصية أو ضبط خاصية [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) للمثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) التي تُرجعها هذه الخاصية إلى قيمة سالبة.

 **Examples:** 

يوضح كيفية ضبط أبعاد الصور كما تقبلها MERGEFIELDS أثناء دمج البريد.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | القيمة المقابلة لـ [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/). |

### setImageStream(InputStream value) {#setImageStream-java.io.InputStream}
```
public void setImageStream(InputStream value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.io.InputStream |  |

### setImageWidth(MergeFieldImageDimension value) {#setImageWidth-com.aspose.words.MergeFieldImageDimension}
```
public void setImageWidth(MergeFieldImageDimension value)
```


يحدد عرض الصورة لإدراجها في المستند.

 **Remarks:** 

القيمة الأولية لهذه الخاصية تأتي من رمز MERGEFIELD المقابل، الموجود في مستند القالب. لتجاوز القيمة الأولية، يجب عليك تعيين مثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) إلى هذه الخاصية أو ضبط الخصائص للمثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) الذي تُرجع هذه الخاصية.

للإشارة إلى أنه يجب تطبيق القيمة الأصلية لعرض الصورة، يجب عليك تعيين القيمة  null  لهذه الخاصية أو ضبط خاصية [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) للمثيل من فئة [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) التي تُرجعها هذه الخاصية إلى قيمة سالبة.

 **Examples:** 

يوضح كيفية ضبط أبعاد الصور كما تقبلها MERGEFIELDS أثناء دمج البريد.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | القيمة المقابلة لـ [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/). |

### setShape(Shape value) {#setShape-com.aspose.words.Shape}
```
public void setShape(Shape value)
```


يحدد الشكل الذي يجب على محرك دمج البريد إدراجه في المستند.

 **Remarks:** 

عند تحديد هذه الخاصية، يتجاهل محرك دمج البريد جميع الخصائص الأخرى مثل [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) أو **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** ويقوم ببساطة بإدراج الشكل في المستند.

استخدم هذه الخاصية للتحكم الكامل في عملية دمج حقل دمج الصورة. على سبيل المثال، يمكنك تحديد [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) أو أي خاصية أخرى للشكل لضبط النود الناتج بدقة. ومع ذلك، يرجى ملاحظة أنك مسؤول عن توفير محتوى الشكل.

 **Examples:** 

يوضح كيفية ضبط أبعاد الصور كما تقبلها MERGEFIELDS أثناء دمج البريد.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape/) | القيمة المقابلة لـ [Shape](../../com.aspose.words/shape/). |

