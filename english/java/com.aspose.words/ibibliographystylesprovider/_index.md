---
title: IBibliographyStylesProvider
linktitle: IBibliographyStylesProvider
second_title: Aspose.Words for Java
description: Implement this interface to provide bibliography style for the FieldBibliography and FieldCitation fields when theyre updated in Java.
type: docs
weight: 673
url: /java/com.aspose.words/ibibliographystylesprovider/
---
```
public interface IBibliographyStylesProvider
```

Implement this interface to provide bibliography style for the [FieldBibliography](../../com.aspose.words/fieldbibliography/) and [FieldCitation](../../com.aspose.words/fieldcitation/) fields when they're updated.

 **Examples:** 

Shows how to override built-in styles or provide custom one.

```

 public void changeBibliographyStyles() throws Exception
 {
     Document doc = new Document(getMyDir() + "Bibliography.docx");

     doc.getFieldOptions().setBibliographyStylesProvider(new BibliographyStylesProvider());
     doc.updateFields();

     doc.save(getArtifactsDir() + "Field.ChangeBibliographyStyles.docx");
 }

 public static class BibliographyStylesProvider implements IBibliographyStylesProvider
 {
     public FileInputStream getStyle(String styleFileName) throws Exception
     {
         return new FileInputStream(getMyDir() + "Bibliography custom style.xsl");
     }
 }
 
```
## Methods

| Method | Description |
| --- | --- |
| [getStyle(String styleFileName)](#getStyle-java.lang.String) | Returns bibliography style. |
### getStyle(String styleFileName) {#getStyle-java.lang.String}
```
public abstract InputStream getStyle(String styleFileName)
```


Returns bibliography style.

 **Remarks:** 

The implementation should return  null  to indicate that the MS Word version of specified style should be used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| styleFileName | java.lang.String | The bibliography style file name. |

**Returns:**
java.io.InputStream - The java.io.InputStream with bibliography style XSLT stylesheet.
