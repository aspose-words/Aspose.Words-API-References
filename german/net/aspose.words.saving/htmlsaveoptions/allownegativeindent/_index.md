---
title: HtmlSaveOptions.AllowNegativeIndent
linktitle: AllowNegativeIndent
articleTitle: AllowNegativeIndent
second_title: Aspose.Words für .NET
description: Entdecken Sie die HtmlSaveOptions AllowNegativeIndent-Eigenschaft zur Steuerung von Absatzeinzügen beim Speichern in HTML, MHTML oder EPUB. Optimieren Sie noch heute Ihre Dokumentformatierung!
type: docs
weight: 20
url: /de/net/aspose.words.saving/htmlsaveoptions/allownegativeindent/
---
## HtmlSaveOptions.AllowNegativeIndent property

Gibt an, ob negative linke und rechte Einzüge von Absätzen beim Speichern in HTML, MHTML oder EPUB normalisiert werden. Der Standardwert ist`FALSCH` .

```csharp
public bool AllowNegativeIndent { get; set; }
```

## Bemerkungen

Wenn ein negativer Einzug nicht zulässig ist, wird er mit Nullrand in HTML exportiert. Wenn ein negativer Einzug zulässig ist, kann ein Absatz teilweise außerhalb des Browserfensters erscheinen.

## Beispiele

Zeigt, wie negative Einrückungen in der HTML-Ausgabe beibehalten werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Tabelle mit negativem Einzug ein, wodurch sie nach links über die linke Seitengrenze hinaus verschoben wird.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Fügen Sie eine Tabelle mit einem positiven Einzug ein, der die Tabelle nach rechts verschiebt.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Wenn wir ein Dokument im HTML-Format speichern, behält Aspose.Words nur negative Einrückungen bei
// wie die, die wir auf die erste Tabelle angewendet haben, wenn wir das Flag „AllowNegativeIndent“ setzen
// in einem SaveOptions-Objekt, das wir an „true“ übergeben.
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

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
