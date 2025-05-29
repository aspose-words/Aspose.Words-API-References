---
title: HtmlElementSizeOutputMode Enum
linktitle: HtmlElementSizeOutputMode
articleTitle: HtmlElementSizeOutputMode
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Saving.HtmlElementSizeOutputMode. Контролируйте размеры элементов для оптимального экспорта HTML, MHTML и EPUB. Улучшите форматирование документов!
type: docs
weight: 5810
url: /ru/net/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enumeration

Указывает, как Aspose.Words экспортирует ширину и высоту элементов в HTML, MHTML и EPUB.

```csharp
public enum HtmlElementSizeOutputMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| All | `0` | Экспортируются все размеры элементов, как в абсолютных, так и в относительных единицах, указанные в документе. |
| RelativeOnly | `1` | Размеры элементов экспортируются только если они указаны в относительных единицах в документе. Фиксированные размеры не экспортируются в этом режиме. Визуальные агенты вычисляют недостающие размеры, чтобы сделать макет документа более естественным. |
| None | `2` | Размеры элементов не экспортируются. Визуальные агенты автоматически построят макет в соответствии с отношениями между элементами. |

## Примеры

Показывает, как сохранить отрицательные отступы в выходном .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте таблицу с отрицательным отступом, который сдвинет ее влево за левую границу страницы.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Вставьте таблицу с положительным отступом, который сдвинет таблицу вправо.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Когда мы сохраняем документ в HTML, Aspose.Words сохранит только отрицательные отступы
// например, тот, который мы применили к первой таблице, если мы установим флаг «AllowNegativeIndent»
// в объекте SaveOptions, которому мы передадим значение «true».
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    AllowNegativeIndent = allowNegativeIndent,
    TableWidthOutputMode = HtmlElementSizeOutputMode.RelativeOnly
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

### Смотрите также

* property [TableWidthOutputMode](../htmlsaveoptions/tablewidthoutputmode/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
