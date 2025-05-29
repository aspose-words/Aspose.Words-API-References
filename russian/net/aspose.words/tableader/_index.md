---
title: TabLeader Enum
linktitle: TabLeader
articleTitle: TabLeader
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.TabLeader, определяющее стили линий выносок для вкладок, улучшающее форматирование документов и удобочитаемость в ваших проектах.
type: docs
weight: 7040
url: /ru/net/aspose.words/tableader/
---
## TabLeader enumeration

Указывает тип линии выноски, отображаемой под символом табуляции.

```csharp
public enum TabLeader
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Линия выноски не отображается. |
| Dots | `1` | Линия выноски состоит из точек. |
| Dashes | `2` | Линия выноски состоит из черточек. |
| Line | `3` | Линия выноски представляет собой одну линию. |
| Heavy | `4` | Линия выноски представляет собой одну толстую линию. |
| MiddleDot | `5` | Линия лидера состоит из средних точек. |

## Примеры

Показывает, как устанавливать пользовательские позиции табуляции для абзаца.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Если мы находимся в абзаце без табуляции в этой коллекции,
// курсор будет перемещаться на 36 пунктов каждый раз при нажатии клавиши Tab в Microsoft Word.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Мы можем добавлять пользовательские позиции табуляции в Microsoft Word, если включим линейку через вкладку «Вид».
// Каждая единица на этой линейке — это две позиции табуляции по умолчанию, что составляет 72 пункта.
// Мы можем добавлять пользовательские позиции табуляции программно, как показано ниже.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Мы можем увидеть эти позиции табуляции в Microsoft Word, включив линейку через «Вид» -> «Показать» -> «Линейка».
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Любые добавляемые нами символы табуляции будут использовать позиции табуляции на линейке и могут,
// в зависимости от значения лидера вкладки, оставьте линию между пунктами отправления и прибытия вкладки.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
