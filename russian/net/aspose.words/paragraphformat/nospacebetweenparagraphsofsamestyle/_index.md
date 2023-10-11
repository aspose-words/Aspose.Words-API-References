---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Когдаистинный SpaceBefore иSpaceAfter будет игнорироваться между абзацами одного стиля.
type: docs
weight: 240
url: /ru/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

Когда`истинный` ,[`SpaceBefore`](../spacebefore/) и[`SpaceAfter`](../spaceafter/) будет игнорироваться между абзацами одного стиля.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

### Примечания

Этот параметр действует только при применении к стилю абзаца. Если применить к абзац напрямую, это не имеет никакого эффекта.

### Примеры

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
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


