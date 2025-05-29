---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.IBibliographyStylesProvider 接口增强您的文档格式，非常适合自定义引用中的参考书目样式。
type: docs
weight: 3080
url: /zh/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

实现此接口来为 提供参考书目样式[`FieldBibliography`](../fieldbibliography/)和[`FieldCitation`](../fieldcitation/)字段更新时。

```csharp
public interface IBibliographyStylesProvider
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | 返回参考书目样式。 |

## 例子

展示如何覆盖内置样式或提供自定义样式。

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // 如果文档已经有样式，您可以使用以下代码进行更改：
    // doc.Bibliography.BibliographyStyle = "书目自定义样式.xsl";

    doc.FieldOptions.BibliographyStylesProvider = new BibliographyStylesProvider();
    doc.UpdateFields();

    doc.Save(ArtifactsDir + "Field.ChangeBibliographyStyles.docx");

}

public class BibliographyStylesProvider : IBibliographyStylesProvider
{
    Stream IBibliographyStylesProvider.GetStyle(string styleFileName)
    {
        return File.OpenRead(MyDir + "Bibliography custom style.xsl");
    }
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
