---
title: "Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders‑metod"
linktitle: "get_ExportImagesForOldReaders"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders‑metod. Anger om nyckelorden för \"old readers\" skrivs till RTF eller inte. Detta kan påverka storleken på RTF‑dokumentet avsevärt. Standardvärdet är true i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/rtfsaveoptions/get_exportimagesforoldreaders/
---
## RtfSaveOptions::get_ExportImagesForOldReaders method


Anger om nyckelorden för "gamla läsare" skrivs till RTF eller inte. Detta kan avsevärt påverka storleken på RTF-dokumentet. Standardvärdet är **true**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders() const
```

## Anmärkningar


"Old readers" är program innan Microsoft Word 97 samt WordPad. När detta alternativ är **true** skriver Aspose.Words ytterligare RTF‑nyckelord. Dessa nyckelord gör att dokumentet visas korrekt när det öppnas i ett "old reader"‑program, men kan avsevärt öka dokumentets storlek.

Om du sätter detta alternativ till **false**, kommer endast bilder i WMF-, EMF- och BMP-format att visas i "old readers".

## Exempel



Visar hur man sparar ett dokument till .rtf med anpassade alternativ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Skapa ett "RtfSaveOptions"-objekt för att skicka till dokumentets "Save"-metod för att ändra hur vi sparar det till en RTF.
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// Ställ in egenskapen "ExportCompactSize" till "true" för att
// minska det sparade dokumentets storlek på bekostnad av kompatibilitet för höger‑till‑vänster text.
options->set_ExportCompactSize(true);

// Ställ in egenskapen "ExportImagesFotOldReaders" till "true" för att använda extra nyckelord för att säkerställa att vårt dokument är
// kompatibelt med läsare för Microsoft Word 97 före och WordPad.
// Ställ in egenskapen "ExportImagesFotOldReaders" till "false" för att minska dokumentets storlek,
// men förhindra att gamla läsare kan läsa några icke‑metafil- eller BMP‑bilder som dokumentet kan innehålla.
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## Se även

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
