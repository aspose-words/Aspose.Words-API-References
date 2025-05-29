---
title: TxtLoadOptions.LeadingSpacesOptions
linktitle: LeadingSpacesOptions
articleTitle: LeadingSpacesOptions
second_title: Aspose.Words for .NET
description: 探索 TxtLoadOptions 的 LeadingSpacesOptions 属性，自定义前导空格处理。使用默认的 ConvertToIndent 设置优化文本加载。
type: docs
weight: 60
url: /zh/net/aspose.words.loading/txtloadoptions/leadingspacesoptions/
---
## TxtLoadOptions.LeadingSpacesOptions property

获取或设置前导空格处理的首选选项。 默认值为ConvertToIndent.

```csharp
public TxtLeadingSpacesOptions LeadingSpacesOptions { get; set; }
```

## 例子

展示如何在加载纯文本文档时修剪空格。

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// 创建一个“TxtLoadOptions”对象，我们可以将其传递给文档的构造函数
// 修改我们加载纯文本文档的方式。
TxtLoadOptions loadOptions = new TxtLoadOptions();

// 将“LeadingSpacesOptions”属性设置为“TxtLeadingSpacesOptions.Preserve”
// 保留每行开头的所有空格字符。
// 将“LeadingSpacesOptions”属性设置为“TxtLeadingSpacesOptions.ConvertToIndent”
// 删除每行开头的所有空格字符，
// 然后对段落应用左首行缩进来模拟空格的效果。
// 将“LeadingSpacesOptions”属性设置为“TxtLeadingSpacesOptions.Trim”
// 从每一行的开头删除所有空格字符。
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// 将“TrailingSpacesOptions”属性设置为“TxtTrailingSpacesOptions.Preserve”
 // 保留每行末尾的所有空格字符。
 // 将“TrailingSpacesOptions”属性设置为“TxtTrailingSpacesOptions.Trim”
// 删除每行末尾的所有空格字符。
loadOptions.TrailingSpacesOptions = txtTrailingSpacesOptions;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

switch (txtLeadingSpacesOptions)
{
    case TxtLeadingSpacesOptions.ConvertToIndent:
        Assert.AreEqual(37.8d, paragraphs[0].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(25.2d, paragraphs[1].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(6.3d, paragraphs[2].ParagraphFormat.FirstLineIndent);

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("      Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("    Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith(" Line 3"));
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1 \r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2   \r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3       \f"));
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1\r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2\r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3\f"));
        break;
}
```

### 也可以看看

* enum [TxtLeadingSpacesOptions](../../txtleadingspacesoptions/)
* class [TxtLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
