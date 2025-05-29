---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words для .NET
description: Откройте для себя метод GetEffectiveTabStops для извлечения всех позиций табуляции в абзаце, включая позиции из стилей и списков для расширенного форматирования.
type: docs
weight: 270
url: /ru/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Возвращает массив всех позиций табуляции, примененных к данному абзацу, включая примененные косвенно стилями или списками.

```csharp
public TabStop[] GetEffectiveTabStops()
```

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

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
