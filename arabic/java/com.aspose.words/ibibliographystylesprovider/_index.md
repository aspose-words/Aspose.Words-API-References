---
title: "IBibliographyStylesProvider"
linktitle: "IBibliographyStylesProvider"
second_title: "Aspose.Words لـ Java"
description: "نفّذ هذه الواجهة لتوفير نمط ببليوغرافي لحقول FieldBibliography و FieldCitation عندما يتم تحديثها في Java."
type: docs
weight: 753
url: /ar/java/com.aspose.words/ibibliographystylesprovider/
---
```
public interface IBibliographyStylesProvider
```

نفّذ هذه الواجهة لتوفير نمط ببليوغرافي لحقول [FieldBibliography](../../com.aspose.words/fieldbibliography/) و [FieldCitation](../../com.aspose.words/fieldcitation/) عندما يتم تحديثها.

 **Examples:** 

يظهر كيفية تجاوز الأنماط المدمجة أو توفير نمط مخصص.

```

 public void changeBibliographyStyles() throws Exception
 {
     Document doc = new Document(getMyDir() + "Bibliography.docx");

     // If the document already has a style you can change it with the following code:
     // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getStyle(String styleFileName)](#getStyle-java.lang.String) | يعيد نمط الببليوغرافيا. |
### getStyle(String styleFileName) {#getStyle-java.lang.String}
```
public abstract InputStream getStyle(String styleFileName)
```


يعيد نمط الببليوغرافيا.

 **Remarks:** 

يجب أن تُعيد التنفيذ  null  للإشارة إلى أنه يجب استخدام نسخة MS Word من النمط المحدد.

 **Examples:** 

يظهر كيفية تجاوز الأنماط المدمجة أو توفير نمط مخصص.

```

 public void changeBibliographyStyles() throws Exception
 {
     Document doc = new Document(getMyDir() + "Bibliography.docx");

     // If the document already has a style you can change it with the following code:
     // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| styleFileName | java.lang.String | اسم ملف نمط الببليوغرافيا. |

**Returns:**
java.io.InputStream - الـ java.io.InputStream مع ورقة أنماط XSLT للببليوغرافيا.
