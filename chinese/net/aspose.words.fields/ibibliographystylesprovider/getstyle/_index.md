---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: Aspose.Words for .NET
description: 探索 IBibliographyStylesProvider GetStyle 方法，轻松检索和自定义参考书目样式，以增强学术写作。
type: docs
weight: 10
url: /zh/net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

返回参考书目样式。

```csharp
public Stream GetStyle(string styleFileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| styleFileName | String | 参考书目样式的文件名。 |

### 返回值

这Stream带有参考书目样式的 XSLT 样式表。

## 评论

实现应该返回`无效的`表示 应使用指定样式的 MS Word 版本。

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

* interface [IBibliographyStylesProvider](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
