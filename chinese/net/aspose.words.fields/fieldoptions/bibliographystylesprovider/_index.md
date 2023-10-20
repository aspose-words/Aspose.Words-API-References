---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: 用于 .NET 的 Aspose.Words
description: FieldOptions BibliographyStylesProvider 财产. 获取或设置返回 的参考书目样式的提供程序FieldBibliography和FieldCitation字段 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

获取或设置返回 的参考书目样式的提供程序[`FieldBibliography`](../../fieldbibliography/)和[`FieldCitation`](../../fieldcitation/)字段.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

## 例子

展示如何覆盖内置样式或提供自定义样式。

```csharp
public void ChangeBibliographyStyles()
{            
    Document doc = new Document(MyDir + "Bibliography.docx");

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

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
