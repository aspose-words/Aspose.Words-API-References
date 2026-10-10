---
title: "Aspose::Words::Saving::PageSet::PageSet‑konstruktor"
linktitle: "PageSet"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PageSet::PageSet‑konstruktor. Skapar en siduppsättning baserad på exakta sidindex i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/pageset/pageset/
---
## PageSet::PageSet(const System::ArrayPtr\<int32_t\>\&) constructor


Skapar en siduppsättning baserad på exakta sidindex.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<int32_t> &pages)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sidor | const System::ArrayPtr\<int32_t\>\& | Nollbaserade index för sidor. |

## Exempel



Visar hur man extraherar sidor baserat på exakta sidindex.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till fem sidor i dokumentet.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod.
// för att ändra hur den metoden konverterar dokumentet till .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Använd egenskapen "PageSet" för att välja en uppsättning av dokumentets sidor som ska sparas till utdata‑XPS.
// I det här fallet kommer vi, via ett nollbaserat index, bara välja tre sidor: sida 1, sida 2 och sida 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Se även

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) constructor


Skapar en siduppsättning baserad på intervall.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Saving::PageRange>> &ranges)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| intervall | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\& | Array av sidintervall. |

## Exempel



Visar hur man extraherar sidor baserat på exakta sidintervall.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Se även

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(int32_t) constructor


Skapar en en-sidig uppsättning baserad på exakt sidindex.

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sida | int32_t | Nollbaserat index för sidan. |

## Exempel



Visar hur man renderar en sida från ett dokument till en JPEG-bild.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Ställ in "PageSet" till "1" för att välja den andra sidan via
// det nollbaserade indexet för att börja rendera dokumentet från.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// När vi sparar dokumentet i JPEG-formatet renderar Aspose.Words bara en sida.
// Denna bild kommer att innehålla en sida som börjar från sida två,
// vilken bara kommer att vara den andra sidan i det ursprungliga dokumentet.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## Se även

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
