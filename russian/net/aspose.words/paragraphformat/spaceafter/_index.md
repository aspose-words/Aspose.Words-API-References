---
title: ParagraphFormat.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words для .NET
description: ParagraphFormat SpaceAfter свойство. Получает или задает величину интервала в пунктах после абзаца на С#.
type: docs
weight: 300
url: /ru/net/aspose.words/paragraphformat/spaceafter/
---
## ParagraphFormat.SpaceAfter property

Получает или задает величину интервала (в пунктах) после абзаца.

```csharp
public double SpaceAfter { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Выдает, когда аргумент выходит за пределы допустимого диапазона значений. |

## Примечания

Не имеет эффекта, когда[`SpaceAfterAuto`](../spaceafterauto/) является`истинный`.

Допустимые значения находятся в диапазоне от 0 до 1584 включительно.

## Примеры

Показывает, как установить автоматический интервал между абзацами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Примените большой интервал до и после абзацев, которые создаст этот конструктор.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Установите для этих флагов значение «true», чтобы применить автоматический интервал,
// эффективно игнорируем интервал в свойствах, которые мы установили выше.
// Оставьте их значение «false», и будет применен наш собственный интервал между абзацами.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Вставьте два абзаца с интервалом выше и ниже и сохраните документ.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

Показывает, как не применять интервалы между абзацами одного стиля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Примените большой интервал до и после абзацев, которые создаст этот конструктор.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Установите для флага «NoSpaceBetweenParagraphsOfSameStyle» значение «true», чтобы применить
// нет интервала между абзацами одного стиля, что позволяет группировать похожие абзацы.
// Оставляем флаг "NoSpaceBetweenParagraphsOfSameStyle" равным "false"
// чтобы равномерно применить интервал к каждому абзацу.
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
