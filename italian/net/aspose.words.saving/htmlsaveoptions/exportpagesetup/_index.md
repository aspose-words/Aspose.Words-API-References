---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ExportPageSetup di HtmlSaveOptions migliora le tue esportazioni HTML, MHTML o EPUB consentendo impostazioni di pagina personalizzabili per un output migliore.
type: docs
weight: 220
url: /it/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Specifica se l'impostazione di pagina viene esportata in HTML, MHTML o EPUB. Il valore predefinito è`falso` .

```csharp
public bool ExportPageSetup { get; set; }
```

## Osservazioni

Ogni[`Section`](../../../aspose.words/section/) nel modello di documento Aspose.Words fornisce informazioni sull'impostazione della pagina tramite[`PageSetup`](../../../aspose.words/pagesetup/) classe. Quando si esporta un documento in formato HTML, potrebbe essere necessario conservare queste informazioni per un utilizzo futuro. In particolare, l'impostazione della pagina potrebbe essere importante per il rendering su supporti impaginati (stampa) o la successiva conversione nei formati di file nativi di Microsoft Word (DOCX, DOC, RTF, WML).

Nella maggior parte dei casi, l'HTML è destinato alla visualizzazione in browser in cui l'impaginazione non viene eseguita. Pertanto, questa feature è disattivata per impostazione predefinita.

## Esempi

Mostra come decidere se conservare le informazioni sulla struttura della sezione/impostazione della pagina durante il salvataggio in HTML.

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

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per decidere se conservare o ignorare le impostazioni di impostazione della pagina.
// Se impostiamo il flag "ExportPageSetup" su "true", il documento HTML di output conterrà la configurazione della nostra pagina.
// Se impostiamo il flag "ExportPageSetup" su "false", l'operazione di salvataggio eliminerà le impostazioni di configurazione della pagina
// per la prima sezione, ed entrambe le sezioni saranno identiche.
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

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
