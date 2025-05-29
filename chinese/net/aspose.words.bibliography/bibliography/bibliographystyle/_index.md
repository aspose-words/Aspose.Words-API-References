---
title: Bibliography.BibliographyStyle
linktitle: BibliographyStyle
articleTitle: BibliographyStyle
second_title: Aspose.Words for .NET
description: 发现 BibliographyStyle 属性可以轻松管理和自定义参考书目的活动样式，以增强组织和展示效果。
type: docs
weight: 10
url: /zh/net/aspose.words.bibliography/bibliography/bibliographystyle/
---
## Bibliography.BibliographyStyle property

获取或设置一个字符串，该字符串表示用于参考书目的活动样式的名称。

```csharp
public string BibliographyStyle { get; set; }
```

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

* class [Bibliography](../)
* 命名空间 [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* 部件 [Aspose.Words](../../../)
