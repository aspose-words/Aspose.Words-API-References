---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: Aspose.Words für .NET
description: HtmlSaveOptions TableWidthOutputMode eigendom. Steuert wie Tabellen Zeilen und Zellenbreiten nach HTML MHTML oder EPUB exportiert werden. Der Standardwert istAll  in C#.
type: docs
weight: 460
url: /de/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Steuert, wie Tabellen-, Zeilen- und Zellenbreiten nach HTML, MHTML oder EPUB exportiert werden. Der Standardwert istAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## Bemerkungen

Im HTML-Format sind Tabellen-, Zeilen- und Zellenelemente (**&lt;Tabelle&gt;** ,**&lt;tr&gt;** ,**&lt;th&gt;** ,**&lt;td&gt;**Die Breite von ) kann entweder in relativen (Prozent) oder in absoluten Einheiten angegeben werden. In einem Dokument in Aspose.Words können die Breiten von Tabellen, Zeilen und Zellen ebenfalls in relativen oder absoluten Einheiten angegeben werden .

Wenn Sie ein Dokument mit Aspose.Words in HTML konvertieren, möchten Sie möglicherweise steuern, wie Tabellen-, Zeilen- und Zellenbreiten exportiert werden, um zu beeinflussen, wie das resultierende Dokument im visuellen Agenten (z. B. einem Browser oder Viewer) angezeigt wird.

Verwenden Sie diese Eigenschaft als Filter, um anzugeben, welche Tabellenbreitenwerte in das Zieldokument exportiert werden. Wenn Sie beispielsweise ein Dokument in EPUB konvertieren und beabsichtigen, das Dokument auf einem mobilen Lesegerät anzuzeigen, , sollten Sie dies wahrscheinlich vermeiden Exportieren absoluter Breitenwerte. Dazu müssen Sie den Ausgabemodus angebenRelativeOnly oderNone , damit der Betrachter auf dem Mobilgerät die Tabelle so gestalten kann, dass sie so gut wie möglich an die Breite des Bildschirms passt.

## Beispiele

Zeigt, wie negative Einzüge in der Ausgabe-.html beibehalten werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Tabelle mit einem negativen Einzug einfügen, wodurch sie nach links über die linke Seitengrenze hinaus verschoben wird.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Fügen Sie eine Tabelle mit einem positiven Einzug ein, wodurch die Tabelle nach rechts verschoben wird.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Wenn wir ein Dokument in HTML speichern, behält Aspose.Words nur negative Einrückungen bei
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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
