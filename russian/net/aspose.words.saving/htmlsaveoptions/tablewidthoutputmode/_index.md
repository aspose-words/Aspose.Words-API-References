---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: Aspose.Words для .NET
description: Оптимизируйте экспорт HTML с помощью HtmlSaveOptions TableWidthOutputMode. Управляйте шириной строк и ячеек таблицы для бесшовного форматирования MHTML и EPUB.
type: docs
weight: 480
url: /ru/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Управляет экспортом ширины таблицы, строк и ячеек в HTML, MHTML или EPUB. Значение по умолчанию:All .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## Примечания

В формате HTML элементы таблицы, строки и ячейки (**&lt;таблица&gt;** ,**&lt;тр&gt;** ,**&lt;й&gt;** ,**&lt;тд&gt;**) может иметь ширину, указанную как в относительных (процентах), так и в абсолютных единицах. В документе Aspose.Words таблицы, строки и ячейки могут иметь ширину, указанную как , используя как относительные, так и абсолютные единицы.

При конвертации документа в HTML с помощью Aspose.Words вам может потребоваться контролировать экспорт ширины таблицы, строк и ячеек, чтобы повлиять на то, как результирующий документ будет отображаться в визуальном агенте (например, браузере или средстве просмотра).

Используйте это свойство как фильтр, чтобы указать, какие значения ширины таблицы экспортируются в целевой документ. Например, если вы конвертируете документ в EPUB и собираетесь просматривать его на мобильном устройстве для чтения, то вы, вероятно, захотите избежать экспорта абсолютных значений ширины. Для этого вам нужно указать режим выводаRelativeOnly илиNone , чтобы зритель на мобильном устройстве мог разместить таблицу так, чтобы она максимально соответствовала ширине экрана.

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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
