---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup HeadingLevelForChapter 财产. 获取或设置应用于文档中章节标题的标题级别样式 在 C#.
type: docs
weight: 180
url: /zh/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

获取或设置应用于文档中章节标题的标题级别样式。

```csharp
public int HeadingLevelForChapter { get; set; }
```

## 评论

可以是 0 到 9 之间的数字。0 表示如果应用于页码则没有章节号。

在创建包含章节编号的页码之前，文档标题必须应用编号大纲格式。

## 例子

展示如何使用页面章节。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
