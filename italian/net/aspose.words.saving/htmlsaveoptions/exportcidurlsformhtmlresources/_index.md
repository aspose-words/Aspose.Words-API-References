---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: Aspose.Words per .NET
description: Scopri come ExportCidUrlsForMhtmlResources di HtmlSaveOptions migliora i documenti MHTML abilitando gli URL CID per immagini, font e CSS. Valore predefinito false.
type: docs
weight: 110
url: /it/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

Specifica se utilizzare URL CID (Content-ID) per fare riferimento a risorse (immagini, font, CSS) incluse nei documenti MHTML . Il valore predefinito è`falso` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## Osservazioni

Questa opzione ha effetto solo sui documenti salvati in formato MHTML.

Per impostazione predefinita, le risorse nei documenti MHTML vengono referenziate tramite il nome del file (ad esempio, "image.png"), which viene confrontato con le intestazioni "Content-Location" delle parti MIME.

Questa opzione abilita un metodo alternativo, in cui i riferimenti ai file di risorse vengono scritti come URL CID (Content-ID) (ad esempio, "cid:image.png") e vengono confrontati con le intestazioni "Content-ID".

In teoria, non dovrebbe esserci alcuna differenza tra i due metodi di riferimento e entrambi dovrebbero funzionare correttamente in qualsiasi browser o agente di posta. In pratica, tuttavia, alcuni agenti non riescono a recuperare le risorse in base al nome del file. Se il browser o l'agente di posta si rifiuta di caricare le risorse incluse in un documento MTHML (non mostra immagini o non carica gli stili CSS), prova a esportare il documento con gli URL CID.

## Esempi

Mostra come abilitare gli ID di contenuto per i documenti MHTML di output.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// L'impostazione di questo flag sostituirà i tag "Content-Location"
// con tag "Content-ID" per ogni risorsa dal documento di input.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mhtml)
{
    ExportCidUrlsForMhtmlResources = exportCidUrlsForMhtmlResources,
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    Assert.True(outDocContents.Contains("Content-ID: <document.html>"));
    Assert.True(outDocContents.Contains("<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    Assert.True(outDocContents.Contains("Content-Location: document.html"));
    Assert.True(outDocContents.Contains("<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
