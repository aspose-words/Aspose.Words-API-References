---
title: "IBibliographyStylesProvider"
linktitle: "IBibliographyStylesProvider"
second_title: "Aspose.Words Java için"
description: "Bu arayüzü, FieldBibliography ve FieldCitation alanları Java'da güncellendiğinde bibliyografi stilini sağlamak için uygulayın."
type: docs
weight: 753
url: /tr/java/com.aspose.words/ibibliographystylesprovider/
---
```
public interface IBibliographyStylesProvider
```

Bu arayüzü, [FieldBibliography](../../com.aspose.words/fieldbibliography/) ve [FieldCitation](../../com.aspose.words/fieldcitation/) alanları güncellendiğinde bibliyografi stilini sağlamak için uygulayın.

 **Examples:** 

Yerleşik stillerin nasıl geçersiz kılınacağını veya özel bir stilin nasıl sağlanacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getStyle(String styleFileName)](#getStyle-java.lang.String) | Bibliyografi stilini döndürür. |
### getStyle(String styleFileName) {#getStyle-java.lang.String}
```
public abstract InputStream getStyle(String styleFileName)
```


Bibliyografi stilini döndürür.

 **Remarks:** 

Uygulama, belirtilen stilin MS Word sürümünün kullanılacağını göstermek için null döndürmelidir.

 **Examples:** 

Yerleşik stillerin nasıl geçersiz kılınacağını veya özel bir stilin nasıl sağlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| styleFileName | java.lang.String | Bibliyografi stil dosyasının adı. |

**Returns:**
java.io.InputStream - Bibliyografya stili XSLT stil sayfasına sahip java.io.InputStream.
