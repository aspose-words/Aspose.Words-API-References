---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ExportPageSetup eigendom. Gibt an ob die Seiteneinrichtung nach HTML MHTML oder EPUB exportiert wird. Die Standardeinstellung istFALSCH  in C#.
type: docs
weight: 220
url: /de/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Gibt an, ob die Seiteneinrichtung nach HTML, MHTML oder EPUB exportiert wird. Die Standardeinstellung ist`FALSCH` .

```csharp
public bool ExportPageSetup { get; set; }
```

## Bemerkungen

Jede[`Section`](../../../aspose.words/section/) Im Aspose.Words-Dokumentmodell werden Seiteneinrichtungsinformationen über bereitgestellt[`PageSetup`](../../../aspose.words/pagesetup/) Klasse. Wenn Sie ein Dokument in das HTML-Format exportieren, müssen Sie diese Informationen möglicherweise für die weitere Verwendung aufbewahren. Insbesondere kann die Seiteneinrichtung für die Wiedergabe auf ausgelagerten Medien (Drucken) oder die anschließende Konvertierung in die nativen Microsoft Word-Dateiformate (DOCX, DOC, RTF, WML) wichtig sein.

In den meisten Fällen ist HTML für die Anzeige in Browsern gedacht, in denen keine Paginierung durchgeführt wird. Daher ist dieses Feature standardmäßig inaktiv.

## Beispiele

Zeigt, wie Sie entscheiden, ob die Abschnittsstruktur/Seiteneinrichtungsinformationen beim Speichern in HTML beibehalten werden sollen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TopMargin = 36.0;
pageSetup.BottomMargin = 36.0;
pageSetup.PaperSize = PaperSize.A5;

// Beim Speichern des Dokuments in HTML können wir ein SaveOptions-Objekt übergeben
// um zu entscheiden, ob die Seiteneinrichtungseinstellungen beibehalten oder verworfen werden sollen.
// Wenn wir das Flag „ExportPageSetup“ auf „true“ setzen, enthält das ausgegebene HTML-Dokument unsere Seiteneinrichtungskonfiguration.
// Wenn wir das Flag „ExportPageSetup“ auf „false“ setzen, verwirft der Speichervorgang unsere Seiteneinrichtungseinstellungen
// für den ersten Abschnitt, und beide Abschnitte werden identisch aussehen.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.True(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" +
        "</style>"));

    Assert.True(outDocContents.Contains(
        "<div class=\"Section_1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));

    Assert.True(outDocContents.Contains(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
