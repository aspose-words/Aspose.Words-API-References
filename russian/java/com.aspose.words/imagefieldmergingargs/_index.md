---
title: "ImageFieldMergingArgs"
linktitle: "ImageFieldMergingArgs"
second_title: "Aspose.Words для Java"
description: "Предоставляет данные для события IFieldMergingCallback.imageFieldMergingcom.aspose.words.ImageFieldMergingArgs в Java."
type: docs
weight: 392
url: /ru/java/com.aspose.words/imagefieldmergingargs/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase/)
```
public class ImageFieldMergingArgs extends FieldMergingArgsBase
```

Предоставляет данные для события [IFieldMergingCallback.imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../../com.aspose.words/ifieldmergingcallback/\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs).

Чтобы узнать больше, посетите статью документации [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Это событие происходит во время слияния почты, когда в документе встречается поле слияния изображения. Вы можете обработать это событие, чтобы вернуть имя файла, поток или объект java.awt.image.BufferedImage движку слияния почты, чтобы он был вставлен в документ.

Доступны три свойства: [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String), **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** и [getImage()](../../com.aspose.words/imagefieldmergingargs/\#getImage) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs/\#setImage-java.awt.image.BufferedImage) для указания источника изображения. Установите только одно из этих свойств.

Чтобы вставить поле слияния изображения в документ Word, выберите команду Вставка/Поле, затем выберите MergeField и введите Image:MyFieldName.

 **Examples:** 

Показывает, как задать размеры изображений, которые MERGEFIELDS принимает во время слияния почты.

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

Показывает, как вставлять изображения, хранящиеся в поле BLOB базы данных, в отчёт.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getDocument()](#getDocument) | Возвращает объект [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument), для которого выполняется слияние почты. |
| [getDocumentFieldName()](#getDocumentFieldName) | Получает имя поля слияния, как указано в документе. |
| [getField()](#getField) | Получает объект, представляющий текущее поле слияния. |
| [getFieldName()](#getFieldName) | Получает имя поля слияния в источнике данных. |
| [getFieldValue()](#getFieldValue) | Получает значение поля из источника данных. |
| [getImage()](#getImage) | Указывает изображение, которое движок слияния почты должен вставить в документ. |
| [getImageFileName()](#getImageFileName) | Устанавливает имя файла изображения, которое движок слияния почты должен вставить в документ. |
| [getImageHeight()](#getImageHeight) | Указывает высоту изображения для вставки в документ. |
| [getImageStream()](#getImageStream) |  |
| [getImageWidth()](#getImageWidth) | Указывает ширину изображения для вставки в документ. |
| [getRecordIndex()](#getRecordIndex) | Получает нулевой индекс записи, которая сливается. |
| [getShape()](#getShape) | Указывает форму, которую движок слияния почты должен вставить в документ. |
| [getTableName()](#getTableName) | Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно. |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object) | Устанавливает значение поля из источника данных. |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage) | Указывает изображение, которое движок слияния почты должен вставить в документ. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Устанавливает имя файла изображения, которое движок слияния почты должен вставить в документ. |
| [setImageHeight(MergeFieldImageDimension value)](#setImageHeight-com.aspose.words.MergeFieldImageDimension) | Указывает высоту изображения для вставки в документ. |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream) |  |
| [setImageWidth(MergeFieldImageDimension value)](#setImageWidth-com.aspose.words.MergeFieldImageDimension) | Указывает ширину изображения для вставки в документ. |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape) | Указывает форму, которую движок слияния почты должен вставить в документ. |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Возвращает объект [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument), для которого выполняется слияние почты.

 **Examples:** 

Показывает, как выполнить слияние почты с пользовательским обратным вызовом, который обрабатывает данные слияния в виде HTML‑документов.

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


Получает имя поля слияния, как указано в документе.

 **Remarks:** 

Если у вас есть сопоставление имени поля документа с другим именем поля в источнике данных, то это оригинальное имя поля, как указано в документе.

Если вы указали префикс имени поля, например "Image:MyFieldName" в документе, то [getDocumentFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getDocumentFieldName) возвращает имя поля без префикса, то есть "MyFieldName".

 **Examples:** 

Показывает, как выполнить слияние почты с пользовательским обратным вызовом, который обрабатывает данные слияния в виде HTML‑документов.

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
java.lang.String — имя поля слияния, как указано в документе.
### getField() {#getField}
```
public FieldMergeField getField()
```


Получает объект, представляющий текущее поле слияния.

 **Examples:** 

Показывает, как выполнить слияние почты с пользовательским обратным вызовом, который обрабатывает данные слияния в виде HTML‑документов.

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


Получает имя поля слияния в источнике данных.

 **Remarks:** 

Если у вас есть сопоставление имени поля документа с другим именем поля в источнике данных, то это сопоставленное имя поля.

Если вы указали префикс имени поля, например "Image:MyFieldName" в документе, то [getFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getFieldName) возвращает имя поля без префикса, то есть "MyFieldName".

 **Examples:** 

Показывает, как вставлять флажковые поля формы в документ во время слияния почты.

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
java.lang.String — имя поля слияния в источнике данных.
### getFieldValue() {#getFieldValue}
```
public Object getFieldValue()
```


Получает значение поля из источника данных.

 **Remarks:** 

Это свойство содержит значение, которое только что было выбрано из вашего источника данных для этого поля движком слияния почты. Вы также можете заменить значение, установив свойство.

 **Examples:** 

Показывает, как использовать значение поля из источника данных.

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
java.lang.Object - Значение поля из источника данных.
### getImage() {#getImage}
```
public BufferedImage getImage()
```


Указывает изображение, которое движок слияния почты должен вставить в документ.

 **Examples:** 

Показывает, как использовать обратный вызов для настройки логики слияния изображений.

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
java.awt.image.BufferedImage — соответствующее значение java.awt.image.BufferedImage.
### getImageFileName() {#getImageFileName}
```
public String getImageFileName()
```


Устанавливает имя файла изображения, которое движок слияния почты должен вставить в документ.

 **Examples:** 

Показывает, как задать размеры изображений, которые MERGEFIELDS принимает во время слияния почты.

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
java.lang.String — имя файла изображения, которое движок слияния почты должен вставить в документ.
### getImageHeight() {#getImageHeight}
```
public MergeFieldImageDimension getImageHeight()
```


Указывает высоту изображения для вставки в документ.

 **Remarks:** 

Значение этого свойства изначально берётся из кода соответствующего MERGEFIELD, содержащегося в шаблоне документа. Чтобы переопределить начальное значение, следует присвоить этому свойству экземпляр класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) или установить свойства для экземпляра класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/), возвращаемого этим свойством.

Чтобы указать, что следует применить оригинальное значение высоты изображения, необходимо присвоить этому свойству значение  null  или установить свойство [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) для экземпляра класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/), возвращаемого этим свойством, в отрицательное значение.

 **Examples:** 

Показывает, как задать размеры изображений, которые MERGEFIELDS принимает во время слияния почты.

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


Указывает ширину изображения для вставки в документ.

 **Remarks:** 

Значение этого свойства изначально берётся из кода соответствующего MERGEFIELD, содержащегося в шаблоне документа. Чтобы переопределить начальное значение, следует присвоить этому свойству экземпляр класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) или установить свойства для экземпляра класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/), возвращаемого этим свойством.

Чтобы указать, что следует применить оригинальное значение ширины изображения, необходимо присвоить этому свойству значение  null  или установить свойство [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) для экземпляра класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/), возвращаемого этим свойством, в отрицательное значение.

 **Examples:** 

Показывает, как задать размеры изображений, которые MERGEFIELDS принимает во время слияния почты.

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


Получает нулевой индекс записи, которая сливается.

 **Examples:** 

Показывает, как вставлять флажковые поля формы в документ во время слияния почты.

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
int - Нулевой индекс записи, которая объединяется.
### getShape() {#getShape}
```
public Shape getShape()
```


Указывает форму, которую движок слияния почты должен вставить в документ.

 **Remarks:** 

Когда это свойство указано, движок слияния почты игнорирует все остальные свойства, такие как [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) или **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream**, и просто вставляет форму в документ.

Используйте это свойство для полного контроля процесса слияния поля изображения. Например, вы можете указать [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) или любое другое свойство формы, чтобы точно настроить полученный узел. Однако обратите внимание, что вы отвечаете за предоставление содержимого формы.

 **Examples:** 

Показывает, как задать размеры изображений, которые MERGEFIELDS принимает во время слияния почты.

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


Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно.

 **Examples:** 

Показывает, как вставлять флажковые поля формы в документ во время слияния почты.

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
java.lang.String - Имя таблицы данных для текущей операции слияния или пустая строка, если имя недоступно.
### setFieldValue(Object value) {#setFieldValue-java.lang.Object}
```
public void setFieldValue(Object value)
```


Устанавливает значение поля из источника данных.

 **Remarks:** 

Это свойство содержит значение, которое только что было выбрано из вашего источника данных для этого поля движком слияния почты. Вы также можете заменить значение, установив свойство.

 **Examples:** 

Показывает, как использовать значение поля из источника данных.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.Object | Значение поля из источника данных. |

### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage value)
```


Указывает изображение, которое движок слияния почты должен вставить в документ.

 **Examples:** 

Показывает, как использовать обратный вызов для настройки логики слияния изображений.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.image.BufferedImage | Соответствующее значение java.awt.image.BufferedImage. |

### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Устанавливает имя файла изображения, которое движок слияния почты должен вставить в документ.

 **Examples:** 

Показывает, как задать размеры изображений, которые MERGEFIELDS принимает во время слияния почты.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя файла изображения, которое движок слияния почты должен вставить в документ. |

### setImageHeight(MergeFieldImageDimension value) {#setImageHeight-com.aspose.words.MergeFieldImageDimension}
```
public void setImageHeight(MergeFieldImageDimension value)
```


Указывает высоту изображения для вставки в документ.

 **Remarks:** 

Значение этого свойства изначально берётся из кода соответствующего MERGEFIELD, содержащегося в шаблоне документа. Чтобы переопределить начальное значение, следует присвоить этому свойству экземпляр класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) или установить свойства для экземпляра класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/), возвращаемого этим свойством.

Чтобы указать, что следует применить оригинальное значение высоты изображения, необходимо присвоить этому свойству значение  null  или установить свойство [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) для экземпляра класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/), возвращаемого этим свойством, в отрицательное значение.

 **Examples:** 

Показывает, как задать размеры изображений, которые MERGEFIELDS принимает во время слияния почты.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | Соответствующее значение [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/). |

### setImageStream(InputStream value) {#setImageStream-java.io.InputStream}
```
public void setImageStream(InputStream value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.io.InputStream |  |

### setImageWidth(MergeFieldImageDimension value) {#setImageWidth-com.aspose.words.MergeFieldImageDimension}
```
public void setImageWidth(MergeFieldImageDimension value)
```


Указывает ширину изображения для вставки в документ.

 **Remarks:** 

Значение этого свойства изначально берётся из кода соответствующего MERGEFIELD, содержащегося в шаблоне документа. Чтобы переопределить начальное значение, следует присвоить этому свойству экземпляр класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) или установить свойства для экземпляра класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/), возвращаемого этим свойством.

Чтобы указать, что следует применить оригинальное значение ширины изображения, необходимо присвоить этому свойству значение  null  или установить свойство [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) для экземпляра класса [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/), возвращаемого этим свойством, в отрицательное значение.

 **Examples:** 

Показывает, как задать размеры изображений, которые MERGEFIELDS принимает во время слияния почты.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | Соответствующее значение [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/). |

### setShape(Shape value) {#setShape-com.aspose.words.Shape}
```
public void setShape(Shape value)
```


Указывает форму, которую движок слияния почты должен вставить в документ.

 **Remarks:** 

Когда это свойство указано, движок слияния почты игнорирует все остальные свойства, такие как [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) или **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream**, и просто вставляет форму в документ.

Используйте это свойство для полного контроля процесса слияния поля изображения. Например, вы можете указать [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) или любое другое свойство формы, чтобы точно настроить полученный узел. Однако обратите внимание, что вы отвечаете за предоставление содержимого формы.

 **Examples:** 

Показывает, как задать размеры изображений, которые MERGEFIELDS принимает во время слияния почты.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape/) | Соответствующее значение [Shape](../../com.aspose.words/shape/). |

