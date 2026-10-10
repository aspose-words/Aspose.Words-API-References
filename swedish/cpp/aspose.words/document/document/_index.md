---
title: "Aspose::Words::Document::Document konstruktor"
linktitle: "Dokument"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::Document konstruktor. Skapar ett tomt Word-dokument i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/document/document/
---
## Document::Document() constructor


Skapar ett tomt Word-dokument.

```cpp
Aspose::Words::Document::Document()
```

## Anmärkningar


Ett tomt dokument hämtas från resurser, och som standard ser det resulterande dokumentet mer ut som skapat av [Word2007](../../../aspose.words.settings/mswordversion/). Detta tomma dokument innehåller en standardteckensnittstabell, minimala standardstilar och latenta stilar.

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

Dokumentets papperstorlek är Letter som standard. Om du vill ändra sidinställningarna, använd [PageSetup](../../section/get_pagesetup/).

Efter skapandet kan du använda [DocumentBuilder](../../documentbuilder/) för att enkelt lägga till dokumentinnehåll.

## Exempel



Visar hur man skapar ett enkelt dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nya Document-objekt innehåller som standard den minsta uppsättningen av noder
// som krävs för att börja lägga till innehåll såsom text och former: en Section, en Body och ett Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


Visar hur man skapar och laddar dokument.
```cpp
// Det finns två sätt att skapa ett Document-objekt med Aspose.Words.
// 1 -  Skapa ett tomt dokument:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nya Document-objekt innehåller som standard den minsta uppsättningen av noder
// som krävs för att börja lägga till innehåll såsom text och former: en Section, en Body och ett Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Ladda ett dokument som finns i det lokala filsystemet:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Laddade dokument kommer att ha innehåll som vi kan komma åt och redigera.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Vissa operationer som måste utföras under laddning, såsom att använda ett lösenord för att dekryptera ett dokument,
// kan göras genom att skicka ett LoadOptions-objekt när dokumentet laddas.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Visar hur man formaterar en run av text med dess font‑egenskap.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Öppnar ett befintligt dokument från en ström. Detekterar automatiskt filformatet.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Ström där dokumentet ska laddas från. |
## Anmärkningar


Dokumentet måste lagras i början av strömmen. Strömmen måste stödja slumpmässig positionering.

## Exempel



Visar hur man laddar ett dokument med en ström.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Öppnar ett befintligt dokument från en ström. Tillåter att specificera ytterligare alternativ såsom ett krypteringslösenord.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Strömmen där dokumentet ska läsas in från. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Ytterligare alternativ att använda när ett dokument läses in. Kan vara **null**. |
## Anmärkningar


Dokumentet måste lagras i början av strömmen. Strömmen måste stödja slumpmässig positionering.

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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


Öppnar ett befintligt dokument från en fil. Detekterar automatiskt filformatet.

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Filnamn på dokumentet som ska öppnas. |

## Exempel



Visar hur man öppnar ett dokument och konverterar det till .PDF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Öppnar ett befintligt dokument från en fil. Tillåter att specificera ytterligare alternativ såsom ett krypteringslösenord.

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Filnamn på dokumentet som ska öppnas. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Ytterligare alternativ att använda när ett dokument läses in. Kan vara **null**. |

## Exempel



Visar hur man skapar och laddar dokument.
```cpp
// Det finns två sätt att skapa ett Document-objekt med Aspose.Words.
// 1 -  Skapa ett tomt dokument:
auto doc = System::MakeObject<Aspose::Words::Document>();

// Nya Document-objekt innehåller som standard den minsta uppsättningen av noder
// som krävs för att börja lägga till innehåll såsom text och former: en Section, en Body och ett Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Ladda ett dokument som finns i det lokala filsystemet:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Laddade dokument kommer att ha innehåll som vi kan komma åt och redigera.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Vissa operationer som måste utföras under laddning, såsom att använda ett lösenord för att dekryptera ett dokument,
// kan göras genom att skicka ett LoadOptions-objekt när dokumentet laddas.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Se även

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
