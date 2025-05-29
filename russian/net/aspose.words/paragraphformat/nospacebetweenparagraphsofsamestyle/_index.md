---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat NoSpaceBetweenParagraphsOfSameStyle. Оптимизируйте макет документа, устранив пробелы между абзацами одного стиля.
type: docs
weight: 250
url: /ru/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

Когда`истинный` ,[`SpaceBefore`](../spacebefore/) и[`SpaceAfter`](../spaceafter/) будет игнорироваться между абзацами одного стиля.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## Примечания

Эта настройка вступает в силу только при применении к стилю абзаца. Если она применяется к абзацу напрямую, она не оказывает никакого эффекта.

## Примеры

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
