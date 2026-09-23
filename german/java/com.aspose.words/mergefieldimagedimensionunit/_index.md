---
title: "MergeFieldImageDimensionUnit"
linktitle: "MergeFieldImageDimensionUnit"
second_title: "Aspose.Words für Java"
description: "Gibt eine Einheit einer Bilddimension an, d. h. in Java."
type: docs
weight: 463
url: /de/java/com.aspose.words/mergefieldimagedimensionunit/
---

**Inheritance:**
java.lang.Object
```
public class MergeFieldImageDimensionUnit
```

Gibt eine Einheit einer Bilddimension an (d. h. die Breite oder die Höhe), die im gesamten Seriendruckvorgang verwendet wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [PERCENT](#PERCENT) | Der Prozentsatz des ursprünglichen Bilddimensionswerts. |
| [POINT](#POINT) | Der Punkt (d. h. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String mergeFieldImageDimensionUnitName)](#fromName-java.lang.String) |  |
| [getName(int mergeFieldImageDimensionUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFieldImageDimensionUnit)](#toString-int) |  |
### PERCENT {#PERCENT}
```
public static int PERCENT
```


Der Prozentsatz des ursprünglichen Bilddimensionswerts.

### POINT {#POINT}
```
public static int POINT
```


Der Punkt (d. h. 1/72 Zoll).

### length {#length}
```
public static int length
```


### fromName(String mergeFieldImageDimensionUnitName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFieldImageDimensionUnitName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mergeFieldImageDimensionUnitName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFieldImageDimensionUnit) {#getName-int}
```
public static String getName(int mergeFieldImageDimensionUnit)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mergeFieldImageDimensionUnit | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFieldImageDimensionUnit) {#toString-int}
```
public static String toString(int mergeFieldImageDimensionUnit)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mergeFieldImageDimensionUnit | int |  |

**Returns:**
java.lang.String
