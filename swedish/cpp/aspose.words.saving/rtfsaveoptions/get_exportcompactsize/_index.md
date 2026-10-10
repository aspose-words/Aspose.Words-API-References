---
title: "Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize‑metod"
linktitle: "get_ExportCompactSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize‑metod. Gör det möjligt att göra utdata‑RTF‑dokument mindre i storlek, men om de innehåller RTL (höger‑till‑vänster) text kommer den inte att visas korrekt. Standardvärdet är falskt i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/rtfsaveoptions/get_exportcompactsize/
---
## RtfSaveOptions::get_ExportCompactSize method


Gör det möjligt att göra utdata‑RTF‑dokument mindre i storlek, men om de innehåller RTL (höger‑till‑vänster) text kommer den inte att visas korrekt. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize() const
```

## Anmärkningar


Om dokumentet som du vill konvertera till RTF med Aspose.Words inte innehåller höger‑till‑vänster‑text på språk som arabiska, kan du sätta detta alternativ till **true** för att minska storleken på den resulterande RTF‑filen.

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
