---
title: ParagraphFormat.SpaceBefore
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает величину интервала в пунктах перед абзацем.
type: docs
weight: 310
url: /ru/net/aspose.words/paragraphformat/spacebefore/
---
## ParagraphFormat.SpaceBefore property

Получает или задает величину интервала (в пунктах) перед абзацем.

```csharp
public double SpaceBefore { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Выдает, когда аргумент находится вне диапазона допустимых значений. |

### Примечания

Не действует, когда[`SpaceBeforeAuto`](../spacebeforeauto/) правда.

Допустимые значения находятся в диапазоне от 0 до 1584 включительно.

### Примеры

Показывает, как установить автоматический интервал между абзацами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Применить большое количество интервалов до и после абзацев, которые создаст этот конструктор.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Установите для этих флагов значение «true», чтобы применить автоматический интервал,
// эффективное игнорирование интервала в свойствах, которые мы установили выше.
// Оставьте их как «false», чтобы применить наш пользовательский интервал между абзацами.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Вставьте два абзаца с интервалами сверху и снизу и сохраните документ.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

Показывает, как применить без интервала между абзацами в одном стиле.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Применить большое количество интервалов до и после абзацев, которые создаст этот конструктор.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Установите для флага "NoSpaceBetweenParagraphsOfSameStyle" значение "true" для применения
// без интервала между абзацами с одинаковым стилем, который будет группировать похожие абзацы.
// Оставляем флаг "NoSpaceBetweenParagraphsOfSameStyle" как "false"
// для равномерного применения интервалов к каждому абзацу.
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


