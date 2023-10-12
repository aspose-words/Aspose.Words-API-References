---
title: PageSetup.RtlGutter
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 获取或设置 Microsoft Word 是否使用基于从右到左语言或从左到右语言的节装订线
type: docs
weight: 380
url: /zh/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

获取或设置 Microsoft Word 是否使用基于从右到左语言或从左到右语言的节装订线。

```csharp
public bool RtlGutter { get; set; }
```

### 例子

展示如何设置装订线边距。

```csharp
Document doc = new Document();

// 插入跨多页的文本。
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// 装订线在左页边距或右页边距中添加空格，
// 这弥补了书中页面居中折叠侵占页面布局的情况。
PageSetup pageSetup = doc.Sections[0].PageSetup;

// 确定页面的边距内有多少文本空间，然后添加一定量来填充边距。
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// 将“RtlGutter”属性设置为“true”，将装订线放置在更适合从右到左文本的位置。
pageSetup.RtlGutter = true;

// 将“MultiplePages”属性设置为“MultiplePagesType.MirrorMargins”以交替
// 每页边距的左/右页边位置。
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


