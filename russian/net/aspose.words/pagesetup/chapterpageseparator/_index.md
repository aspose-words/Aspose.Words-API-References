---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words для .NET
description: PageSetup ChapterPageSeparator свойство. Получает или задает символразделитель который появляется между номером главы и номером страницы на С#.
type: docs
weight: 90
url: /ru/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Получает или задает символ-разделитель, который появляется между номером главы и номером страницы.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## Примечания

Прежде чем вы сможете создавать номера страниц, включающие номера глав, к заголовкам документов необходимо применить нумерованный структурный формат.

## Примеры

Показывает, как работать с главами страниц.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Смотрите также

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
