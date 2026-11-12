---
title: "IBibliographyStylesProvider"
linktitle: "IBibliographyStylesProvider"
second_title: "Aspose.Words для Java"
description: "Реализуйте этот интерфейс, чтобы предоставить стиль библиографии для полей FieldBibliography и FieldCitation, когда они обновляются в Java."
type: docs
weight: 753
url: /ru/java/com.aspose.words/ibibliographystylesprovider/
---
```
public interface IBibliographyStylesProvider
```

Реализуйте этот интерфейс, чтобы предоставить стиль библиографии для полей [FieldBibliography](../../com.aspose.words/fieldbibliography/) и [FieldCitation](../../com.aspose.words/fieldcitation/), когда они обновляются.

 **Examples:** 

Показывает, как переопределить встроенные стили или предоставить пользовательский.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getStyle(String styleFileName)](#getStyle-java.lang.String) | Возвращает стиль библиографии. |
### getStyle(String styleFileName) {#getStyle-java.lang.String}
```
public abstract InputStream getStyle(String styleFileName)
```


Возвращает стиль библиографии.

 **Remarks:** 

Реализация должна возвращать  null , чтобы указать, что следует использовать версию стиля MS Word.

 **Examples:** 

Показывает, как переопределить встроенные стили или предоставить пользовательский.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| styleFileName | java.lang.String | Имя файла стиля библиографии. |

**Returns:**
java.io.InputStream — java.io.InputStream с XSLT‑шаблоном в стиле библиографии.
