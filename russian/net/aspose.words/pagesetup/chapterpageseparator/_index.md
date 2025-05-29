---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChapterPageSeparator в PageSetup. Легко настройте символ-разделитель между номерами глав и страниц для изысканного вида.
type: docs
weight: 90
url: /ru/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Возвращает или задает символ разделителя, который отображается между номером главы и номером страницы.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## Примечания

Прежде чем создавать номера страниц, включающие номера глав, к заголовкам документа необходимо применить формат нумерованной структуры.

## Примеры

Показывает, как работать с главами страницы.

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
