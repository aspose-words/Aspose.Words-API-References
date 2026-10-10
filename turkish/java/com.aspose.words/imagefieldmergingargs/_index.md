---
title: "ImageFieldMergingArgs"
linktitle: "ImageFieldMergingArgs"
second_title: "Aspose.Words Java için"
description: "Java'da IFieldMergingCallback.imageFieldMergingcom.aspose.words.ImageFieldMergingArgs olayı için veri sağlar."
type: docs
weight: 392
url: /tr/java/com.aspose.words/imagefieldmergingargs/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase/)
```
public class ImageFieldMergingArgs extends FieldMergingArgsBase
```

Bu, [IFieldMergingCallback.imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../../com.aspose.words/ifieldmergingcallback/\\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs) olayı için veri sağlar.

Daha fazla bilgi edinmek için, [ Mail Merge and Reporting ][Mail Merge and Reporting] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu olay, posta birleştirme sırasında belgede bir görüntü posta birleştirme alanı bulunduğunda gerçekleşir. Bu olaya yanıt vererek bir dosya adı, akış veya bir java.awt.image.BufferedImage nesnesi döndürebilir ve böylece posta birleştirme motoru tarafından belgeye eklenir.

Kullanılabilir üç özellik vardır: [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\\#setImageFileName-java.lang.String), **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** ve [getImage()](../../com.aspose.words/imagefieldmergingargs/\\#getImage) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs/\\#setImage-java.awt.image.BufferedImage) - görüntünün nereden alınacağını belirtir. Bu özelliklerden yalnızca birini ayarlayın.

Word'de bir belgeye görüntü posta birleştirme alanı eklemek için Ekle/Alan komutunu seçin, ardından BirleştirmeAlanı'nı seçin ve Image:MyFieldName yazın.

 **Examples:** 

Posta birleştirme sırasında MERGEFIELDS'in kabul ettiği şekilde görüntü boyutlarını nasıl ayarlayacağınızı gösterir.

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

Veritabanı BLOB alanında depolanan görüntülerin bir rapora nasıl ekleneceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDocument()](#getDocument) | Posta birleştirme işleminin gerçekleştirildiği [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) nesnesini döndürür. |
| [getDocumentFieldName()](#getDocumentFieldName) | Belgede belirtilen birleştirme alanının adını alır. |
| [getField()](#getField) | Geçerli birleştirme alanını temsil eden nesneyi alır. |
| [getFieldName()](#getFieldName) | Veri kaynağındaki birleştirme alanının adını alır. |
| [getFieldValue()](#getFieldValue) | Alan değerini veri kaynağından alır. |
| [getImage()](#getImage) | Belirtilen görüntüyü posta birleştirme motorunun belgeye eklemesi gerekir. |
| [getImageFileName()](#getImageFileName) | Posta birleştirme motorunun belgeye eklemesi gereken görüntünün dosya adını ayarlar. |
| [getImageHeight()](#getImageHeight) | Belgeye eklenecek görüntünün yüksekliğini belirtir. |
| [getImageStream()](#getImageStream) |  |
| [getImageWidth()](#getImageWidth) | Belgeye eklenecek görüntünün genişliğini belirtir. |
| [getRecordIndex()](#getRecordIndex) | Birleştirilen kaydın sıfır tabanlı indeksini alır. |
| [getShape()](#getShape) | Posta birleştirme motorunun belgeye eklemesi gereken şekli belirtir. |
| [getTableName()](#getTableName) | Geçerli birleştirme işlemi için veri tablosunun adını alır; ad mevcut değilse boş string döndürür. |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object) | Alan değerini veri kaynağından ayarlar. |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage) | Belirtilen görüntüyü posta birleştirme motorunun belgeye eklemesi gerekir. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Posta birleştirme motorunun belgeye eklemesi gereken görüntünün dosya adını ayarlar. |
| [setImageHeight(MergeFieldImageDimension value)](#setImageHeight-com.aspose.words.MergeFieldImageDimension) | Belgeye eklenecek görüntünün yüksekliğini belirtir. |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream) |  |
| [setImageWidth(MergeFieldImageDimension value)](#setImageWidth-com.aspose.words.MergeFieldImageDimension) | Belgeye eklenecek görüntünün genişliğini belirtir. |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape) | Posta birleştirme motorunun belgeye eklemesi gereken şekli belirtir. |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Posta birleştirme işleminin gerçekleştirildiği [getDocument()](../../com.aspose.words/fieldmergingargsbase/\#getDocument) nesnesini döndürür.

 **Examples:** 

HTML belgeleri biçiminde birleştirme verilerini işleyen özel bir geri arama ile posta birleştirme nasıl yürütülür gösterir.

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


Belgede belirtilen birleştirme alanının adını alır.

 **Remarks:** 

Eğer bir belge alan adı ile farklı bir veri kaynağı alan adı arasında bir eşleme varsa, bu belge içinde belirtilen orijinal alan adıdır.

Belgede örneğin \"Image:MyFieldName\" gibi bir alan adı öneki belirttiyseniz, [getDocumentFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getDocumentFieldName) önek olmadan alan adını döndürür; bu da \"MyFieldName\" olur.

 **Examples:** 

HTML belgeleri biçiminde birleştirme verilerini işleyen özel bir geri arama ile posta birleştirme nasıl yürütülür gösterir.

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
java.lang.String - Belgede belirtilen birleştirme alanının adı.
### getField() {#getField}
```
public FieldMergeField getField()
```


Geçerli birleştirme alanını temsil eden nesneyi alır.

 **Examples:** 

HTML belgeleri biçiminde birleştirme verilerini işleyen özel bir geri arama ile posta birleştirme nasıl yürütülür gösterir.

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


Veri kaynağındaki birleştirme alanının adını alır.

 **Remarks:** 

Eğer bir belge alan adı ile farklı bir veri kaynağı alan adı arasında bir eşleme varsa, bu eşlenmiş alan adıdır.

Belgede örneğin \"Image:MyFieldName\" gibi bir alan adı öneki belirttiyseniz, [getFieldName()](../../com.aspose.words/fieldmergingargsbase/\#getFieldName) önek olmadan alan adını döndürür; bu da \"MyFieldName\" olur.

 **Examples:** 

Posta birleştirme sırasında bir belgeye onay kutusu form alanları eklemenin nasıl yapılacağını gösterir.

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
java.lang.String - Veri kaynağındaki birleştirme alanının adı.
### getFieldValue() {#getFieldValue}
```
public Object getFieldValue()
```


Alan değerini veri kaynağından alır.

 **Remarks:** 

Bu özellik, posta birleştirme motoru tarafından bu alan için veri kaynağınızdan yeni seçilen bir değeri içerir. Özelliği ayarlayarak değeri değiştirebilirsiniz.

 **Examples:** 

Alanının veri kaynağı değerinin nasıl kullanılacağını gösterir.

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
java.lang.Object - Veri kaynağından alanın değeri.
### getImage() {#getImage}
```
public BufferedImage getImage()
```


Belirtilen görüntüyü posta birleştirme motorunun belgeye eklemesi gerekir.

 **Examples:** 

Görüntü birleştirme mantığını özelleştirmek için bir geri aramanın nasıl kullanılacağını gösterir.

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
java.awt.image.BufferedImage - İlgili java.awt.image.BufferedImage değeri.
### getImageFileName() {#getImageFileName}
```
public String getImageFileName()
```


Posta birleştirme motorunun belgeye eklemesi gereken görüntünün dosya adını ayarlar.

 **Examples:** 

Posta birleştirme sırasında MERGEFIELDS'in kabul ettiği şekilde görüntü boyutlarını nasıl ayarlayacağınızı gösterir.

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
java.lang.String - Posta birleştirme motorunun belgeye eklemesi gereken görüntünün dosya adı.
### getImageHeight() {#getImageHeight}
```
public MergeFieldImageDimension getImageHeight()
```


Belgeye eklenecek görüntünün yüksekliğini belirtir.

 **Remarks:** 

Bu özelliğin değeri başlangıçta şablon belgesinde bulunan ilgili MERGEFIELD kodundan gelir. Başlangıç değerini geçersiz kılmak için bu özelliğe bir [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneğini atamalı veya bu özellik tarafından döndürülen [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneği için özellikleri ayarlamalısınız.

Görüntü yüksekliğinin orijinal değerinin uygulanmasını göstermek için bu özelliğe  null  değerini atamalı veya bu özellik tarafından döndürülen [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneği için [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) özelliğini negatif bir değere ayarlamalısınız.

 **Examples:** 

Posta birleştirme sırasında MERGEFIELDS'in kabul ettiği şekilde görüntü boyutlarını nasıl ayarlayacağınızı gösterir.

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


Belgeye eklenecek görüntünün genişliğini belirtir.

 **Remarks:** 

Bu özelliğin değeri başlangıçta şablon belgesinde bulunan ilgili MERGEFIELD kodundan gelir. Başlangıç değerini geçersiz kılmak için bu özelliğe bir [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneğini atamalı veya bu özellik tarafından döndürülen [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneği için özellikleri ayarlamalısınız.

Görüntü genişliğinin orijinal değerinin uygulanmasını göstermek için bu özelliğe  null  değerini atamalı veya bu özellik tarafından döndürülen [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneği için [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) özelliğini negatif bir değere ayarlamalısınız.

 **Examples:** 

Posta birleştirme sırasında MERGEFIELDS'in kabul ettiği şekilde görüntü boyutlarını nasıl ayarlayacağınızı gösterir.

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


Birleştirilen kaydın sıfır tabanlı indeksini alır.

 **Examples:** 

Posta birleştirme sırasında bir belgeye onay kutusu form alanları eklemenin nasıl yapılacağını gösterir.

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
int - Birleştirilen kaydın sıfır tabanlı indeksi.
### getShape() {#getShape}
```
public Shape getShape()
```


Posta birleştirme motorunun belgeye eklemesi gereken şekli belirtir.

 **Remarks:** 

Bu özellik belirtildiğinde, posta birleştirme motoru [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) veya **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** gibi diğer tüm özellikleri yok sayar ve yalnızca şekli belgeye ekler.

Bu özelliği bir görüntü birleştirme alanının birleştirme sürecini tam olarak kontrol etmek için kullanın. Örneğin, sonuç düğümünü ince ayarlamak için [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) veya başka bir şekil özelliğini belirtebilirsiniz. Ancak, şeklin içeriğini sağlamaktan sizin sorumlu olduğunuzu lütfen unutmayın.

 **Examples:** 

Posta birleştirme sırasında MERGEFIELDS'in kabul ettiği şekilde görüntü boyutlarını nasıl ayarlayacağınızı gösterir.

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


Geçerli birleştirme işlemi için veri tablosunun adını alır; ad mevcut değilse boş string döndürür.

 **Examples:** 

Posta birleştirme sırasında bir belgeye onay kutusu form alanları eklemenin nasıl yapılacağını gösterir.

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
java.lang.String - Mevcut birleştirme işlemi için veri tablosunun adı veya ad mevcut değilse boş dize.
### setFieldValue(Object value) {#setFieldValue-java.lang.Object}
```
public void setFieldValue(Object value)
```


Alan değerini veri kaynağından ayarlar.

 **Remarks:** 

Bu özellik, posta birleştirme motoru tarafından bu alan için veri kaynağınızdan yeni seçilen bir değeri içerir. Özelliği ayarlayarak değeri değiştirebilirsiniz.

 **Examples:** 

Alanının veri kaynağı değerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.Object | Veri kaynağından alanın değeri. |

### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage value)
```


Belirtilen görüntüyü posta birleştirme motorunun belgeye eklemesi gerekir.

 **Examples:** 

Görüntü birleştirme mantığını özelleştirmek için bir geri aramanın nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.image.BufferedImage | İlgili java.awt.image.BufferedImage değeri. |

### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Posta birleştirme motorunun belgeye eklemesi gereken görüntünün dosya adını ayarlar.

 **Examples:** 

Posta birleştirme sırasında MERGEFIELDS'in kabul ettiği şekilde görüntü boyutlarını nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Posta birleştirme motorunun belgeye eklemesi gereken görüntünün dosya adı. |

### setImageHeight(MergeFieldImageDimension value) {#setImageHeight-com.aspose.words.MergeFieldImageDimension}
```
public void setImageHeight(MergeFieldImageDimension value)
```


Belgeye eklenecek görüntünün yüksekliğini belirtir.

 **Remarks:** 

Bu özelliğin değeri başlangıçta şablon belgesinde bulunan ilgili MERGEFIELD kodundan gelir. Başlangıç değerini geçersiz kılmak için bu özelliğe bir [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneğini atamalı veya bu özellik tarafından döndürülen [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneği için özellikleri ayarlamalısınız.

Görüntü yüksekliğinin orijinal değerinin uygulanmasını göstermek için bu özelliğe  null  değerini atamalı veya bu özellik tarafından döndürülen [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneği için [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) özelliğini negatif bir değere ayarlamalısınız.

 **Examples:** 

Posta birleştirme sırasında MERGEFIELDS'in kabul ettiği şekilde görüntü boyutlarını nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | İlgili [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) değeri. |

### setImageStream(InputStream value) {#setImageStream-java.io.InputStream}
```
public void setImageStream(InputStream value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.io.InputStream |  |

### setImageWidth(MergeFieldImageDimension value) {#setImageWidth-com.aspose.words.MergeFieldImageDimension}
```
public void setImageWidth(MergeFieldImageDimension value)
```


Belgeye eklenecek görüntünün genişliğini belirtir.

 **Remarks:** 

Bu özelliğin değeri başlangıçta şablon belgesinde bulunan ilgili MERGEFIELD kodundan gelir. Başlangıç değerini geçersiz kılmak için bu özelliğe bir [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneğini atamalı veya bu özellik tarafından döndürülen [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneği için özellikleri ayarlamalısınız.

Görüntü genişliğinin orijinal değerinin uygulanmasını göstermek için bu özelliğe  null  değerini atamalı veya bu özellik tarafından döndürülen [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) sınıfının örneği için [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) özelliğini negatif bir değere ayarlamalısınız.

 **Examples:** 

Posta birleştirme sırasında MERGEFIELDS'in kabul ettiği şekilde görüntü boyutlarını nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) | İlgili [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension/) değeri. |

### setShape(Shape value) {#setShape-com.aspose.words.Shape}
```
public void setShape(Shape value)
```


Posta birleştirme motorunun belgeye eklemesi gereken şekli belirtir.

 **Remarks:** 

Bu özellik belirtildiğinde, posta birleştirme motoru [getImageFileName()](../../com.aspose.words/imagefieldmergingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs/\#setImageFileName-java.lang.String) veya **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** gibi diğer tüm özellikleri yok sayar ve yalnızca şekli belgeye ekler.

Bu özelliği bir görüntü birleştirme alanının birleştirme sürecini tam olarak kontrol etmek için kullanın. Örneğin, sonuç düğümünü ince ayarlamak için [ShapeBase.getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) veya başka bir şekil özelliğini belirtebilirsiniz. Ancak, şeklin içeriğini sağlamaktan sizin sorumlu olduğunuzu lütfen unutmayın.

 **Examples:** 

Posta birleştirme sırasında MERGEFIELDS'in kabul ettiği şekilde görüntü boyutlarını nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape/) | İlgili [Shape](../../com.aspose.words/shape/) değeri. |

