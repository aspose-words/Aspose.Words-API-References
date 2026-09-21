---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages metod"
linktitle: "get_ExportEmbeddedImages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages metod. Anger om bilder ska bäddas in i Html‑dokumentet i Base64‑format. Observera att inställning av denna flagga kan öka storleken på den genererade Html‑filen avsevärt i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


Anger om bilder ska bäddas in i Html-dokumentet i Base64-format. Observera att inställning av denna flagga kan avsevärt öka storleken på den genererade Html-filen.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## Exempel



Visar hur man bestämmer var bilder ska lagras när ett dokument exporteras till Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// När vi exporterar ett dokument med inbäddade bilder till .html,
// Aspose.Words kan placera bilderna på två möjliga platser.
// Att sätta flaggan "ExportEmbeddedImages" till "true" kommer att lagra den råa datan
// för alla bilder i det genererade HTML‑dokumentet, i "src"‑attributet för <image>-taggar.
// Att sätta denna flagga till "false" kommer att skapa en bildfil i det lokala filsystemet för varje bild,
// och lagra alla dessa filer i en separat mapp.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## Se även

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
