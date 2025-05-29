---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup HeadingLevelForChapter, которое позволяет легко настраивать стили заголовков глав в документе для повышения читабельности и профессионализма.
type: docs
weight: 180
url: /ru/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Возвращает или задает стиль уровня заголовка, применяемый к заголовкам глав в документе.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## Примечания

Может быть числом от 0 до 9. 0 означает отсутствие номера главы, если он применен к номеру страницы.

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

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
