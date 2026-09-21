---
title: "Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions konstruktor"
linktitle: "HtmlLoadOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions konstruktor. Initierar en ny instans av denna klass med standardvärden i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


Initierar en ny instans av den här klassen med standardvärden.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
```


## Exempel



Visar hur man stödjer villkorliga kommentarer vid inläsning av ett HTML-dokument.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Om värdet är sant, tar vi VML-kod i beaktande när vi parsar det laddade dokumentet.
loadOptions->set_SupportVml(supportVml);

// Detta dokument innehåller en JPEG-bild inom "<!--[if gte vml 1]>"-taggar,
// och en annan PNG-bild inom "<![if !vml]>"-taggar.
// Om vi sätter flaggan "SupportVml" till "true" kommer Aspose.Words att ladda JPEG-filen.
// Om vi sätter denna flagga till "false" kommer Aspose.Words endast att ladda PNG-filen.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Se även

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


En genväg för att initiera en ny instans av den här klassen med egenskaper satta till de angivna värdena.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
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
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| password | const System::String\& | Lösenordet för att öppna ett krypterat dokument. Kan vara **null** eller en tom sträng. |

## Exempel



Visar hur man krypterar ett Html-dokument och sedan öppnar det med ett lösenord.
```cpp
// Skapa och signera ett krypterat HTML-dokument från en krypterad .docx.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"HtmlLoadOptions.EncryptedHtml.html";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// För att ladda och läsa detta dokument måste vi skicka dess dekryptering
// lösenord med ett HtmlLoadOptions-objekt.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = System::MakeObject<Aspose::Words::Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## Se även

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
