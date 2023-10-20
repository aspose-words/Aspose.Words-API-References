---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: Aspose.Words для .NET
description: PageSetup HeadingLevelForChapter свойство. Получает или задает стиль уровня заголовка который применяется к заголовкам глав в документе на С#.
type: docs
weight: 180
url: /ru/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Получает или задает стиль уровня заголовка, который применяется к заголовкам глав в документе.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## Примечания

Может быть числом от 0 до 9. 0 означает отсутствие номера главы, если оно применяется к номеру страницы.

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

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
