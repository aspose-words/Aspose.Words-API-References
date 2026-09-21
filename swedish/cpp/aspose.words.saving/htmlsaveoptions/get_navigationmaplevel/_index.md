---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel metod"
linktitle: "get_NavigationMapLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel metod. Anger den maximala nivån av rubriker som fylls i navigationskartan vid export till EPUB-, MOBI- eller AZW3-format. Standardvärdet är %3 i C++."
type: docs
weight: 40500
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


Anger den maximala nivån av rubriker som fylls i navigeringskartan när man exporterar till EPUB-, MOBI- eller AZW3‑format. Standardvärdet är **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## Anmärkningar


Navigeringskartan låter användaragenter att erbjuda ett enkelt sätt att navigera genom dokumentstrukturen. Vanligtvis motsvarar navigeringspunkter rubriker i dokumentet. För att fylla i rubriker upp till nivå **N** tilldelar du detta värde till [NavigationMapLevel](./).

Som standard fylls tre nivåer av rubriker i: stycken med stilarna **Heading 1**, **Heading 2** och **Heading 3**. Du kan sätta denna egenskap till ett värde mellan 1 och 9 för att begära motsvarande maximala nivå. Att sätta den till noll kommer att reducera navigeringskartan till endast dokumentroten eller rötterna för dokumentdelar.

## Exempel



Visar hur man genererar innehållsförteckning för Azw3-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Azw3);
options->set_NavigationMapLevel(2);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```


Visar hur man genererar innehållsförteckning för Mobi-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mobi);
options->set_NavigationMapLevel(5);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateMobiToc.mobi", options);
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
