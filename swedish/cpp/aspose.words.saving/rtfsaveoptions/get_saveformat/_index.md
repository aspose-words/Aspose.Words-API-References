---
title: "Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat‑metod"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat‑metod. Anger det format i vilket dokumentet kommer att sparas om detta sparalternativ‑objekt används. Kan endast vara Rtf i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/rtfsaveoptions/get_saveformat/
---
## RtfSaveOptions::get_SaveFormat method


Anger det format i vilket dokumentet kommer att sparas om detta sparalternativ‑objekt används. Kan endast vara [Rtf](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
