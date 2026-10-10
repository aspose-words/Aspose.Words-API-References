---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup metodo"
linktitle: "get_ExportPageSetup"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup metodo. Specifica se la configurazione della pagina viene esportata in HTML, MHTML o EPUB. Il valore predefinito è false in C++."
type: docs
weight: 24000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


Specifica se la configurazione della pagina viene esportata in HTML, MHTML o EPUB. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## Note


Ogni [Section](../../../aspose.words/section/) nel modello di documento Aspose.Words fornisce le informazioni di configurazione della pagina tramite la classe [PageSetup](../../../aspose.words/pagesetup/). Quando esporti un documento in formato HTML potresti aver bisogno di conservare queste informazioni per un uso successivo. In particolare, la configurazione della pagina potrebbe essere importante per il rendering su supporti paginati (stampa) o per la conversione successiva nei formati nativi di Microsoft Word (DOCX, DOC, RTF, WML).

Nella maggior parte dei casi l'HTML è destinato alla visualizzazione nei browser dove la paginazione non viene eseguita. Pertanto questa funzionalità è inattiva per impostazione predefinita.

## Esempi



Mostra come decidere se preservare le informazioni sulla struttura delle sezioni/configurazione della pagina durante il salvataggio in HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TopMargin(36.0);
pageSetup->set_BottomMargin(36.0);
pageSetup->set_PaperSize(Aspose::Words::PaperSize::A5);

// Quando si salva il documento in HTML, possiamo passare un oggetto SaveOptions
// per decidere se preservare o scartare le impostazioni di configurazione della pagina.
// Se impostiamo il flag "ExportPageSetup" su "true", il documento HTML di output conterrà la nostra configurazione di impostazione della pagina.
// Se impostiamo il flag "ExportPageSetup" su "false", l'operazione di salvataggio scarterà le nostre impostazioni di configurazione della pagina
// per la prima sezione, e entrambe le sezioni appariranno identiche.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageSetup(exportPageSetup);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<style type=\"text/css\">") + u"@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" + u"</style>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div class=\"Section_1\">") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div>") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
