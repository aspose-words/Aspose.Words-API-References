---
title: "MergeFieldImageDimensionUnit"
linktitle: "MergeFieldImageDimensionUnit"
second_title: "Aspose.Words para Java"
description: "Especifica una unidad de una dimensión de imagen, p.ej. en Java."
type: docs
weight: 463
url: /es/java/com.aspose.words/mergefieldimagedimensionunit/
---

**Inheritance:**
java.lang.Object
```
public class MergeFieldImageDimensionUnit
```

Especifica una unidad de una dimensión de imagen (p.ej. el ancho o la altura) utilizada en un proceso de combinación de correspondencia.

 **Examples:** 

Muestra cómo establecer las dimensiones de las imágenes que los MERGEFIELDS aceptan durante una combinación de correspondencia.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [PERCENT](#PERCENT) | El porcentaje del valor original de la dimensión de la imagen. |
| [POINT](#POINT) | El punto (p.ej. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String mergeFieldImageDimensionUnitName)](#fromName-java.lang.String) |  |
| [getName(int mergeFieldImageDimensionUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFieldImageDimensionUnit)](#toString-int) |  |
### PERCENT {#PERCENT}
```
public static int PERCENT
```


El porcentaje del valor original de la dimensión de la imagen.

### POINT {#POINT}
```
public static int POINT
```


El punto (p.ej. 1/72 de pulgada).

### length {#length}
```
public static int length
```


### fromName(String mergeFieldImageDimensionUnitName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFieldImageDimensionUnitName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mergeFieldImageDimensionUnitName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFieldImageDimensionUnit) {#getName-int}
```
public static String getName(int mergeFieldImageDimensionUnit)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mergeFieldImageDimensionUnit | int |  |

**Returns:**
java.lang.String
