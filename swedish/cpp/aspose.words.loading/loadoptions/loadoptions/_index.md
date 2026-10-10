---
title: "Aspose::Words::Loading::LoadOptions::LoadOptions konstruktör"
linktitle: "LoadOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::LoadOptions konstruktör. Initierar en ny instans av denna klass med standardvärden i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


Initierar en ny instans av den här klassen med standardvärden.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


## Exempel



Visar hur man öppnar ett HTML-dokument med bilder från en ström med hjälp av en bas-URI.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Skicka med URI:n för basmappen när du laddar den
    // så att eventuella bilder med relativa URI:er i HTML-dokumentet kan hittas.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Verifiera att den första formen i dokumentet innehåller en giltig bild.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Se även

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


En genväg för att initiera en ny instans av den här klassen med egenskaper satta till de angivna värdena.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | Formatet på dokumentet som ska laddas. |
| password | const System::String\& | Lösenordet för att öppna ett krypterat dokument. Kan vara **null** eller en tom sträng. |
| baseUri | const System::String\& | Strängen som kommer att användas för att lösa relativa URI:er till absoluta. Kan vara **null** eller en tom sträng. |

## Exempel



Visar hur man anger en bas‑URI när man öppnar ett html‑dokument.
```cpp
// Anta att vi vill läsa in ett .html‑dokument som innehåller en bild länkad med en relativ URI
// medan bilden finns på en annan plats. I så fall måste vi omvandla den relativa URI:n till en absolut.
// Vi kan ange en bas‑URI med ett HtmlLoadOptions‑objekt.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Även om bilden var trasig i den inmatade .html‑filen, hjälpte vår anpassade bas‑URI oss att reparera länken.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Detta utdata‑dokument kommer att visa bilden som saknades.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Se även

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(const System::String\&) constructor


En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| password | const System::String\& | Lösenordet för att öppna ett krypterat dokument. Kan vara **null** eller en tom sträng. |

## Exempel



Visar hur man laddar ett krypterat Microsoft Word-dokument.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words kastar ett undantag om vi försöker öppna ett krypterat dokument utan dess lösenord.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// När ett sådant dokument laddas, skickas lösenordet till dokumentets konstruktor med ett LoadOptions-objekt.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Det finns två sätt att ladda ett krypterat dokument med ett LoadOptions-objekt.
// 1 -  Ladda dokumentet från det lokala filsystemet med filnamn:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Ladda dokumentet från en ström:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Se även

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
