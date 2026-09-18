---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources Methode"
linktitle: "get_ExportCidUrlsForMhtmlResources"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources Methode. Gibt an, ob CID (Content-ID)-URLs verwendet werden sollen, um Ressourcen (Bilder, Schriftarten, CSS) in MHTML‑Dokumenten zu referenzieren. Standardwert ist false in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


Gibt an, ob CID (Content-ID)-URLs verwendet werden sollen, um Ressourcen (Bilder, Schriftarten, CSS) zu referenzieren, die in MHTML-Dokumenten enthalten sind. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## Hinweise


Diese Option wirkt nur bei Dokumenten, die als MHTML gespeichert werden.

Standardmäßig werden Ressourcen in MHTML‑Dokumenten über den Dateinamen referenziert (z. B. "image.png"), der mit den "Content-Location"‑Headern von MIME‑Teilen abgeglichen wird.

Diese Option ermöglicht eine alternative Methode, bei der Verweise auf Ressourcendateien als CID (Content-ID)-URLs geschrieben werden (z. B. "cid:image.png") und mit den "Content-ID"‑Headern abgeglichen werden.

Theoretisch sollte es keinen Unterschied zwischen den beiden Referenzierungsmethoden geben und beide sollten in jedem Browser oder Mail‑Client einwandfrei funktionieren. In der Praxis jedoch scheitern einige Clients beim Abrufen von Ressourcen über den Dateinamen. Wenn Ihr Browser oder Mail‑Client die in einem MTHML‑Dokument enthaltenen Ressourcen nicht lädt (zeigt keine Bilder oder lädt keine CSS‑Stile), versuchen Sie, das Dokument mit CID‑URLs zu exportieren.

## Beispiele



Zeigt, wie Content‑IDs für ausgegebene MHTML‑Dokumente aktiviert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Durch Setzen dieses Flags werden "Content-Location"‑Tags ersetzt
// durch "Content-ID"‑Tags für jede Ressource aus dem Eingabedokument.
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

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
