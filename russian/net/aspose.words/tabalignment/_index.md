---
title: TabAlignment Enum
linktitle: TabAlignment
articleTitle: TabAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.TabAlignment для настраиваемого выравнивания табуляции. Улучшите форматирование документов с точностью и гибкостью уже сегодня!
type: docs
weight: 7030
url: /ru/net/aspose.words/tabalignment/
---
## TabAlignment enumeration

Указывает выравнивание/тип позиции табуляции.

```csharp
public enum TabAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Left | `0` | Выравнивает текст после позиции табуляции по левому краю. |
| Center | `1` | Центрирует текст вокруг позиции табуляции. |
| Right | `2` | Выравнивает текст по правому краю на позиции табуляции. |
| Decimal | `3` | Выравнивает текст по десятичной точке. |
| Bar | `4` | Рисует вертикальную черту в позиции табуляции. |
| List | `6` | Табуляция является разделителем между номером/маркером и текстом в элементе списка. |
| Clear | `7` | Удаляет любую позицию табуляции в этой позиции. |

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
