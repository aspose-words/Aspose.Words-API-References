---
title: "MergeFieldImageDimension"
linktitle: "MergeFieldImageDimension"
second_title: "Aspose.Words لـ Java"
description: "يمثل أبعاد الصورة أي في Java."
type: docs
weight: 462
url: /ar/java/com.aspose.words/mergefieldimagedimension/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MergeFieldImageDimension implements Cloneable
```

يمثل أبعاد الصورة (أي العرض أو الارتفاع) المستخدمة عبر عملية دمج البريد.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fields ][Working with Fields].

 **Remarks:** 

للإشارة إلى أنه يجب إدراج الصورة بأبعادها الأصلية أثناء دمج البريد، يجب عليك تعيين قيمة سالبة لخاصية [getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double).

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


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [MergeFieldImageDimension(double value)](#MergeFieldImageDimension-double) | ينشئ كائن أبعاد الصورة بالقيمة المعطاة بالنقاط. |
| [MergeFieldImageDimension(double value, int unit)](#MergeFieldImageDimension-double-int) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getUnit()](#getUnit) | الوحدة. |
| [getValue()](#getValue) | القيمة. |
| [setUnit(int value)](#setUnit-int) | الوحدة. |
| [setValue(double value)](#setValue-double) | القيمة. |
### MergeFieldImageDimension(double value) {#MergeFieldImageDimension-double}
```
public MergeFieldImageDimension(double value)
```


ينشئ كائن أبعاد الصورة بالقيمة المعطاة بالنقاط.

 **Remarks:** 

يجب عليك استخدام قيمة سالبة للإشارة إلى أنه يجب تطبيق القيمة الأصلية لأبعاد الصورة المقابلة.

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
| قيمة | double | القيمة. |

### MergeFieldImageDimension(double value, int unit) {#MergeFieldImageDimension-double-int}
```
public MergeFieldImageDimension(double value, int unit)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double |  |
| unit | int |  |

### getUnit() {#getUnit}
```
public int getUnit()
```


الوحدة.

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
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit/).
### getValue() {#getValue}
```
public double getValue()
```


القيمة.

 **Remarks:** 

يجب عليك استخدام قيمة سالبة للإشارة إلى أنه يجب تطبيق القيمة الأصلية لأبعاد الصورة المقابلة.

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
double - القيمة المقابلة للـ double.
### setUnit(int value) {#setUnit-int}
```
public void setUnit(int value)
```


الوحدة.

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
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit/). |

### setValue(double value) {#setValue-double}
```
public void setValue(double value)
```


القيمة.

 **Remarks:** 

يجب عليك استخدام قيمة سالبة للإشارة إلى أنه يجب تطبيق القيمة الأصلية لأبعاد الصورة المقابلة.

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
| قيمة | double | القيمة العشرية المقابلة. |

