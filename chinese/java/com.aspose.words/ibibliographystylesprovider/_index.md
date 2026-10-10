---
title: "IBibliographyStylesProvider"
linktitle: "IBibliographyStylesProvider"
second_title: "Aspose.Words for Java"
description: "在 Java 中实现此接口，以在 FieldBibliography 和 FieldCitation 字段更新时提供参考文献样式。"
type: docs
weight: 753
url: /zh/java/com.aspose.words/ibibliographystylesprovider/
---
```
public interface IBibliographyStylesProvider
```

实现此接口，以在 [FieldBibliography](../../com.aspose.words/fieldbibliography/) 和 [FieldCitation](../../com.aspose.words/fieldcitation/) 字段更新时提供参考文献样式。

 **Examples:** 

展示如何覆盖内置样式或提供自定义样式。

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
## 方法

| 方法 | 描述 |
| --- | --- |
| [getStyle(String styleFileName)](#getStyle-java.lang.String) | 返回参考文献样式。 |
### getStyle(String styleFileName) {#getStyle-java.lang.String}
```
public abstract InputStream getStyle(String styleFileName)
```


返回参考文献样式。

 **Remarks:** 

实现应该返回  null  以指示应使用指定样式的 MS Word 版本。

 **Examples:** 

展示如何覆盖内置样式或提供自定义样式。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| styleFileName | java.lang.String | 参考文献样式文件名。 |

**Returns:**
`java.io.InputStream` - 包含参考文献样式 XSLT 样式表的 java.io.InputStream。
