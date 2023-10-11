---
title: PageSetup.ChapterPageSeparator
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 获取或设置出现在章节号和页码之间的分隔符
type: docs
weight: 90
url: /zh/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

获取或设置出现在章节号和页码之间的分隔符。

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

### 评论

在创建包含章节编号的页码之前，文档标题必须应用编号大纲格式。

### 例子

展示如何使用页面章节。

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
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


