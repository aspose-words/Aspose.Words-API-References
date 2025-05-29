---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Aufzählung „TxtExportHeadersFootersMode“ von Aspose.Words den Export von reinem Text verbessert, indem sie die Kopf- und Fußzeilenbehandlung für optimale Ergebnisse anpasst.
type: docs
weight: 6440
url: /de/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

Gibt an, wie Kopf- und Fußzeilen in das Nur-Text-Format exportiert werden.

```csharp
public enum TxtExportHeadersFootersMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Es werden keine Kopf- und Fußzeilen exportiert. |
| PrimaryOnly | `1` | Es werden nur primäre Kopf- und Fußzeilen am Anfang und Ende jedes Abschnitts exportiert. |
| AllAtEnd | `2` | Alle Kopf- und Fußzeilen werden nach allen Abschnittstexten ganz am Ende eines Dokuments platziert. |

## Beispiele

Zeigt, wie Sie angeben, wie Kopf- und Fußzeilen in das Nur-Text-Format exportiert werden.

```csharp
Document doc = new Document();

// Fügen Sie gleichmäßige und primäre Kopf-/Fußzeilen in das Dokument ein.
// Die primären Kopf-/Fußzeilen überschreiben die geraden Kopf-/Fußzeilen.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Seiten einfügen, um diese Kopf- und Fußzeilen anzuzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Setzen Sie die Eigenschaft „ExportHeadersFootersMode“ auf „TxtExportHeadersFootersMode.None“
// um keine Kopf-/Fußzeilen zu exportieren.
// Setzen Sie die Eigenschaft „ExportHeadersFootersMode“ auf „TxtExportHeadersFootersMode.PrimaryOnly“
// um nur primäre Kopf-/Fußzeilen zu exportieren.
// Setzen Sie die Eigenschaft „ExportHeadersFootersMode“ auf „TxtExportHeadersFootersMode.AllAtEnd“
// um alle Kopf- und Fußzeilen für alle Abschnittstexte am Ende des Dokuments zu platzieren.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

string newLine = Environment.NewLine;
switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Even header{newLine}{newLine}" +
                        $"Primary header{newLine}{newLine}" +
                        $"Even footer{newLine}{newLine}" +
                        $"Primary footer{newLine}{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual($"Primary header{newLine}" +
                        $"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Primary footer{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}", docText);
        break;
}
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
