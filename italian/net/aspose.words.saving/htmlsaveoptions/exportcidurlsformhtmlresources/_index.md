---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ExportCidUrlsForMhtmlResources proprietà. Specifica se utilizzare gli URL CID ContentID per fare riferimento alle risorse immagini caratteri CSS incluse nei documenti MHTML . Il valore predefinito èfalso  in C#.
type: docs
weight: 110
url: /it/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

Specifica se utilizzare gli URL CID (Content-ID) per fare riferimento alle risorse (immagini, caratteri, CSS) incluse nei documenti MHTML . Il valore predefinito è`falso` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## Osservazioni

Questa opzione influisce solo sui documenti salvati in MHTML.

Per impostazione predefinita, alle risorse nei documenti MHTML viene fatto riferimento tramite il nome file (ad esempio, "image.png"), che viene confrontato con le intestazioni "Content-Location" delle parti MIME.

Questa opzione abilita un metodo alternativo, in cui i riferimenti ai file di risorse vengono scritti come URL CID (Content-ID) (ad esempio, "cid:image.png") e vengono confrontati con le intestazioni "Content-ID".

In teoria, non dovrebbero esserci differenze tra i due metodi di riferimento e entrambi dovrebbero funzionare bene in qualsiasi browser o agente di posta. In pratica, tuttavia, alcuni agenti non riescono a recuperare le risorse in base al nome del file. Se il tuo browser o agente di posta si rifiuta di caricare le risorse incluse in un documento MTHML (non mostra immagini o non carica stili CSS), prova a esportare il documento con URL CID.

## Esempi

Mostra come abilitare gli ID contenuto per i documenti MHTML di output.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// L'impostazione di questo flag sostituirà i tag "Content-Location".
// con tag "Content-ID" per ciascuna risorsa dal documento di input.
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
