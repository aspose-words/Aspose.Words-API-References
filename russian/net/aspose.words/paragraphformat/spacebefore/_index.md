---
title: ParagraphFormat.SpaceBefore
linktitle: SpaceBefore
articleTitle: SpaceBefore
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat SpaceBefore, которое позволяет легко настраивать интервалы между абзацами в пунктах, улучшая читабельность и стиль документа.
type: docs
weight: 330
url: /ru/net/aspose.words/paragraphformat/spacebefore/
---
## ParagraphFormat.SpaceBefore property

Возвращает или задает величину интервала (в пунктах) перед абзацем.

```csharp
public double SpaceBefore { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызывается, когда аргумент выходит за пределы допустимых значений. |

## Примечания

Не имеет никакого эффекта, когда[`SpaceBeforeAuto`](../spacebeforeauto/) является`истинный`.

Допустимые значения находятся в диапазоне от 0 до 1584 включительно.

## Примеры

Показывает, как установить автоматический интервал между абзацами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Применить большой интервал до и после абзацев, которые создаст этот конструктор.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Установите эти флаги на «true», чтобы применить автоматический интервал,
// фактически игнорируя интервал в свойствах, которые мы установили выше.
// Если оставить значение "false", будет применен наш пользовательский интервал между абзацами.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Вставьте два абзаца с интервалами сверху и снизу и сохраните документ.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

Показывает, как не использовать интервалы между абзацами с одинаковым стилем.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Применить большой интервал до и после абзацев, которые создаст этот конструктор.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Установите флаг "NoSpaceBetweenParagraphsOfSameStyle" на "true", чтобы применить
// без интервала между абзацами с одинаковым стилем, что позволит сгруппировать похожие абзацы.
// Оставьте флаг "NoSpaceBetweenParagraphsOfSameStyle" как "false"
// для равномерного применения интервала к каждому абзацу.
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
