---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method"
linktitle: "get_ExportCidUrlsForMhtmlResources"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method. Specifica se utilizzare URL CID (Content-ID) per fare riferimento alle risorse (immagini, font, CSS) incluse nei documenti MHTML. Il valore predefinito è false in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


Specifica se utilizzare URL CID (Content-ID) per fare riferimento alle risorse (immagini, font, CSS) incluse nei documenti MHTML. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## Note


Questa opzione influisce solo sui documenti salvati in MHTML.

Per impostazione predefinita, le risorse nei documenti MHTML sono referenziate per nome file (ad esempio, \"image.png\"), che vengono confrontate con le intestazioni \"Content-Location\" delle parti MIME.

Questa opzione abilita un metodo alternativo, in cui i riferimenti ai file di risorsa sono scritti come URL CID (Content-ID) (ad esempio, \"cid:image.png\") e sono confrontati con le intestazioni \"Content-ID\".

In teoria, non dovrebbe esserci alcuna differenza tra i due metodi di riferimento e entrambi dovrebbero funzionare correttamente in qualsiasi browser o client di posta. In pratica, tuttavia, alcuni client non riescono a recuperare le risorse per nome file. Se il tuo browser o client di posta rifiuta di caricare le risorse incluse in un documento MTHML (non mostra le immagini o non carica gli stili CSS), prova a esportare il documento con URL CID.

## Esempi



Mostra come abilitare gli ID di contenuto per i documenti MHTML di output.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Impostare questo flag sostituirà i tag \"Content-Location\"
// con i tag \"Content-ID\" per ogni risorsa del documento di input.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mhtml);
options->set_ExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-ID: <document.html>"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-Location: document.html"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
