---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words для .NET
description: Aspose.Words.ChapterPageSeparator перечисление. Определяет символразделитель который появляется между главой и номером страницы на С#.
type: docs
weight: 200
url: /ru/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Определяет символ-разделитель, который появляется между главой и номером страницы.

```csharp
public enum ChapterPageSeparator
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Hyphen | `0` | Двоеточие. |
| Period | `1` | Точка. |
| Colon | `2` | Двоеточие. |
| EmDash | `3` | Подчеркнутое тире. |
| EnDash | `4` | Стандартное тире. |

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

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
