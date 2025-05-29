---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre HTML-Exporte mit dem HtmlSaveOptions TableWidthOutputMode. Steuern Sie die Zeilen- und Zellenbreite der Tabelle für eine nahtlose MHTML- und EPUB-Formatierung.
type: docs
weight: 480
url: /de/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Steuert, wie Tabellen-, Zeilen- und Zellenbreiten in HTML, MHTML oder EPUB exportiert werden. Der Standardwert istAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## Bemerkungen

Im HTML-Format sind Tabellen-, Zeilen- und Zellenelemente (**&lt;Tabelle&gt;** ,**&lt;tr&gt;** ,**&lt;th&gt;** ,**&lt;td&gt;**) Die Breite kann entweder in relativen (Prozent) oder in absoluten Einheiten angegeben werden. In einem Dokument in Aspose.Words kann die Breite von Tabellen, Zeilen und Zellen ebenfalls in relativen oder absoluten Einheiten angegeben werden.

Wenn Sie ein Dokument mit Aspose.Words in HTML konvertieren, möchten Sie möglicherweise steuern, wie Tabellen-, Zeilen- und Zellenbreiten exportiert werden, um die Anzeige des resultierenden Dokuments im visuellen Agenten (z. B. einem Browser oder Viewer) zu beeinflussen.

Verwenden Sie diese Eigenschaft als Filter, um festzulegen, welche Tabellenbreiten in das Zieldokument exportiert werden sollen. Wenn Sie beispielsweise ein Dokument ins EPUB-Format konvertieren und es auf einem mobilen Lesegerät anzeigen möchten, sollten Sie den Export absoluter Breitenwerte vermeiden. Geben Sie dazu den Ausgabemodus an.RelativeOnly oderNone , damit der Betrachter auf dem Mobilgerät die Tabelle optimal an die Bildschirmbreite anpassen kann.

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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
