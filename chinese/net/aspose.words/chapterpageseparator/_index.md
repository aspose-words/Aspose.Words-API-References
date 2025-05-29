---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ChapterPageSeparator 枚举以自定义章节和页码分隔符，从而增强文档格式和清晰度。
type: docs
weight: 390
url: /zh/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

定义章节和页码之间的分隔符。

```csharp
public enum ChapterPageSeparator
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Hyphen | `0` | 冒号。 |
| Period | `1` | 一个句号。 |
| Colon | `2` | 冒号。 |
| EmDash | `3` | 强调破折号。 |
| EnDash | `4` | 标准破折号。 |

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

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
