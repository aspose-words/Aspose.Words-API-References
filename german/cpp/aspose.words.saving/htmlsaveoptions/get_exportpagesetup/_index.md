---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup Methode"
linktitle: "get_ExportPageSetup"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup Methode. Gibt an, ob die Seiteneinrichtung in HTML, MHTML oder EPUB exportiert wird. Standard ist false in C++."
type: docs
weight: 24000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


Gibt an, ob die Seiteneinrichtung nach HTML, MHTML oder EPUB exportiert wird. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## Hinweise


Jeder [Section](../../../aspose.words/section/) im Aspose.Words-Dokumentenmodell liefert Seiteneinrichtungsinformationen über die Klasse [PageSetup](../../../aspose.words/pagesetup/). Wenn Sie ein Dokument in das HTML-Format exportieren, müssen Sie diese Informationen möglicherweise für die weitere Verwendung behalten. Insbesondere kann die Seiteneinrichtung für die Darstellung auf paginierten Medien (Druck) oder die anschließende Konvertierung in die nativen Microsoft‑Word-Dateiformate (DOCX, DOC, RTF, WML) wichtig sein.

In den meisten Fällen ist HTML für die Anzeige in Browsern vorgesehen, in denen keine Seitennummerierung erfolgt. Daher ist diese Funktion standardmäßig deaktiviert.

## Beispiele



Zeigt, wie entschieden wird, ob die Abschnittsstruktur/Seiteneinrichtungsinformationen beim Speichern nach HTML erhalten bleiben sollen.
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

// Beim Speichern des Dokuments als HTML können wir ein SaveOptions‑Objekt übergeben
// um zu entscheiden, ob Seiteneinrichtungseinstellungen beibehalten oder verworfen werden sollen.
// Wenn wir das Flag "ExportPageSetup" auf "true" setzen, enthält das ausgegebene HTML‑Dokument unsere Seiteneinrichtungskonfiguration.
// Wenn wir das Flag "ExportPageSetup" auf "false" setzen, verwirft der Speicher­vorgang unsere Seiteneinrichtungseinstellungen
// für den ersten Abschnitt, und beide Abschnitte sehen identisch aus.
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

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
