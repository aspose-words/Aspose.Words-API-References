---
title: DocumentBuilder.PageSetup
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 财产. 返回一个表示当前页面设置和节属性的对象
type: docs
weight: 160
url: /zh/net/aspose.words/documentbuilder/pagesetup/
---
## DocumentBuilder.PageSetup property

返回一个表示当前页面设置和节属性的对象。

```csharp
public PageSetup PageSetup { get; }
```

### 例子

演示如何将页面设置设置应用和恢复到文档中的各个部分。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 修改构建器当前部分的页面设置属性并添加文本。
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// 如果我们使用文档生成器开始一个新部分，
// 它将继承构建器的当前页面设置属性。
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// 我们可以使用“ClearFormatting”方法将其页面设置属性恢复为其默认值。
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### 也可以看看

* class [PageSetup](../../pagesetup/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


