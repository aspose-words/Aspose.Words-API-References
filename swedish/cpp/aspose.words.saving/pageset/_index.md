---
title: "Aspose::Words::Saving::PageSet class"
linktitle: "PageSet"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PageSet-klass. Beskriver en slumpmässig uppsättning sidor. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words.saving/pageset/
---
## PageSet class


Beskriver en slumpmässig uppsättning sidor. För att lära dig mer, besök dokumentationsartikeln [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [get_All](./get_all/)() | Hämtar en uppsättning med alla dokumentets sidor i deras ursprungliga ordning. |
| static [get_Even](./get_even/)() | Hämtar en uppsättning med alla jämna sidor i dokumentet i deras ursprungliga ordning. |
| static [get_Odd](./get_odd/)() | Hämtar en uppsättning med alla udda sidor i dokumentet i deras ursprungliga ordning. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | Skapar en en-sidig uppsättning baserad på exakt sidindex. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Skapar en siduppsättning baserad på exakta sidindex. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Skapar en siduppsättning baserad på intervall. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
