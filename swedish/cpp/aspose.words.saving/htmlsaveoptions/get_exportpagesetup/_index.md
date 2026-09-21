---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup metod"
linktitle: "get_ExportPageSetup"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup‑metod. Anger om sidinställningar exporteras till HTML, MHTML eller EPUB. Standardvärdet är falskt i C++."
type: docs
weight: 24000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


Anger om sidinställningar exporteras till HTML, MHTML eller EPUB. Standard är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## Anmärkningar


Varje [Section](../../../aspose.words/section/) i Aspose.Words-dokumentmodellen tillhandahåller sidinställningsinformation via klassen [PageSetup](../../../aspose.words/pagesetup/) . När du exporterar ett dokument till HTML‑format kan du behöva behålla denna information för vidare användning. I synnerhet kan sidinställningar vara viktiga för rendering till paginerade medier (utskrift) eller efterföljande konvertering till de ursprungliga Microsoft Word‑filformaten (DOCX, DOC, RTF, WML).

I de flesta fall är HTML avsedd för visning i webbläsare där paginering inte utförs. Så denna funktion är inaktiv som standard.

## Exempel



Visar hur man bestämmer om sektionens struktur/sidinställningsinformation ska bevaras vid sparande till HTML.
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

// När dokumentet sparas till HTML kan vi skicka ett SaveOptions‑objekt
// för att avgöra om sidinställningsinställningarna ska bevaras eller kasseras.
// Om vi sätter flaggan "ExportPageSetup" till "true" kommer den genererade HTML‑dokumentet att innehålla vår sidinställningskonfiguration.
// Om vi sätter flaggan "ExportPageSetup" till "false" kommer sparningsoperationen att kassera våra sidinställningsinställningar.
// för den första sektionen, och båda sektionerna kommer att se identiska ut.
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

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
