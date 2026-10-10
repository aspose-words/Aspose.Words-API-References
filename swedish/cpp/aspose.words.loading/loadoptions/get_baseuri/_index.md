---
title: "Aspose::Words::Loading::LoadOptions::get_BaseUri metod"
linktitle: "get_BaseUri"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_BaseUri metod. Hämtar eller anger strängen som kommer att användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er när det behövs. Kan vara null eller en tom sträng. Standardvärdet är null i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.loading/loadoptions/get_baseuri/
---
## LoadOptions::get_BaseUri method


Hämtar eller anger strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er när det behövs. Kan vara **null** eller en tom sträng. Standardvärdet är **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_BaseUri() const
```

## Anmärkningar


Denna egenskap används för att lösa relativa URI:er till absoluta i följande fall:

1. Vid inläsning av ett HTML-dokument från en ström och dokumentet innehåller bilder med relativa URI:er och saknar en bas-URI som specificerats i BASE‑HTML‑elementet.
1. Vid sparande av ett dokument till PDF och andra format, för att hämta bilder som länkas med relativa URI:er så att bilderna kan sparas i utdata‑dokumentet.



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
