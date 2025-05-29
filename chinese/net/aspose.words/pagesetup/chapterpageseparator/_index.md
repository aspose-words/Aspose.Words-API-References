---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words for .NET
description: 在 PageSetup 中探索 ChapterPageSeparator 属性。轻松自定义章节和页码之间的分隔符，打造更美观的外观。
type: docs
weight: 90
url: /zh/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

获取或设置章节号和页码之间的分隔符。

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## 评论

在创建包含章节号的页码之前，文档标题必须应用编号大纲格式。

## 例子

展示如何处理页面章节。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### 也可以看看

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
