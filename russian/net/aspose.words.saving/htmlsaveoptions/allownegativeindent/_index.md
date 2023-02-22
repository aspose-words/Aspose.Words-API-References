---
title: HtmlSaveOptions.AllowNegativeIndent
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает нормализуются ли отрицательные отступы слева и справа абзацев при сохранении в HTML MHTML или EPUB. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 20
url: /ru/net/aspose.words.saving/htmlsaveoptions/allownegativeindent/
---
## HtmlSaveOptions.AllowNegativeIndent property

Указывает, нормализуются ли отрицательные отступы слева и справа абзацев при сохранении в HTML, MHTML или EPUB. Значение по умолчанию`ЛОЖЬ` .

```csharp
public bool AllowNegativeIndent { get; set; }
```

### Примечания

Если отрицательный отступ не разрешен, он экспортируется как нулевое поле в HTML. Если разрешен отрицательный отступ, абзац может частично отображаться за пределами окна браузера .

### Примеры

Показывает, как сохранить отрицательные отступы в выходном .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить таблицу с отрицательным отступом, который сдвинет ее влево за левую границу страницы.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Вставить таблицу с положительным отступом, который сдвинет таблицу вправо.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Когда мы сохраняем документ в HTML, Aspose.Words сохранит только отрицательные отступы
// такой же, как тот, который мы применили к первой таблице, если мы установили флаг "AllowNegativeIndent"
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

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


