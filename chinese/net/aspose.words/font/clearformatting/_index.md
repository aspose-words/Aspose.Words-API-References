---
title: Font.ClearFormatting
second_title: Aspose.Words for .NET API 参考
description: Font 方法. 重置为默认字体格式
type: docs
weight: 550
url: /zh/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

重置为默认字体格式。

```csharp
public void ClearFormatting()
```

### 评论

删除在which 对象上显式指定的所有字体格式[`Font`](../)已获得，因此字体格式将从 适当的父级继承。

### 例子

演示如何插入超链接字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// 插入超链接并使用自定义格式强调它。
// 超链接将是一段可点击的文本，它将带我们到 URL 中指定的位置。
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + 左键单击 Microsoft Word 中文本中的链接将通过新的 Web 浏览器窗口转到 URL。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


