---
title: Interface IBibliographyStylesProvider
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.IBibliographyStylesProvider 界面. 实现此接口为 提供参考书目样式FieldBibliography和FieldCitation更新时的字段
type: docs
weight: 2670
url: /zh/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

实现此接口为 提供参考书目样式[`FieldBibliography`](../fieldbibliography/)和[`FieldCitation`](../fieldcitation/)更新时的字段。

```csharp
public interface IBibliographyStylesProvider
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(string) | 返回参考书目样式。 |

### 例子

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

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


