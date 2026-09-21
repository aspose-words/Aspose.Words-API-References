---
title: "Aspose::Words::Drawing::SignatureLine class"
linktitle: "SignatureLine"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::SignatureLine class. Tillhandahåller åtkomst till egenskaper för signaturlinje. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


Ger åtkomst till egenskaper för signaturlinje. För att lära dig mer, besök dokumentationsartikeln [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLine : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | Hämtar eller anger ett värde som indikerar att undertecknaren kan lägga till kommentarer i Sign-dialogen. Standardvärdet för denna egenskap är **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() | Hämtar eller anger ett värde som indikerar att standardinstruktioner visas i Sign-dialogen. Standardvärdet för denna egenskap är **true**. |
| [get_Email](./get_email/)() | Hämtar eller anger föreslagen undertecknares e‑postadress. Standardvärdet för denna egenskap är **empty string**. |
| [get_Id](./get_id/)() | Hämtar eller anger identifieraren för denna signaturlinje. Denna identifierare kan associeras med en digital signatur när dokumentet signeras med [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/). Detta värde måste vara unikt och som standard genereras ett nytt Guid slumpmässigt (**NewGuid**). |
| [get_Instructions](./get_instructions/)() | Hämtar eller anger instruktioner till undertecknaren som visas vid signering av signaturlinjen. Denna egenskap ignoreras om [DefaultInstructions](./get_defaultinstructions/) är angiven. Standardvärdet för denna egenskap är **empty string**. |
| [get_IsSigned](./get_issigned/)() | Indikerar att signaturlinjen är signerad med en digital signatur. |
| [get_IsValid](./get_isvalid/)() | Indikerar att signaturlinjen är signerad med en digital signatur och att denna digitala signatur är giltig. |
| [get_ProviderId](./get_providerid/)() | Hämtar eller anger signaturleverantörens identifierare för den här signaturlinjen. Standardvärdet är "{00000000-0000-0000-0000-000000000000}". |
| [get_ShowDate](./get_showdate/)() | Hämtar eller anger ett värde som indikerar att signeringsdatum visas i signaturlinjen. Standardvärdet för denna egenskap är **true**. |
| [get_Signer](./get_signer/)() | Hämtar eller anger föreslagen undertecknare för signaturlinjen. Standardvärdet för denna egenskap är **empty string**. |
| [get_SignerTitle](./get_signertitle/)() | Hämtar eller anger föreslagen undertecknares titel (till exempel Chef). Standardvärdet för denna egenskap är **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Sättare för [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Sättare för [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/). |
| [set_Id](./set_id/)(System::Guid) | Sättare för [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Sättare för [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/). |
| [set_ShowDate](./set_showdate/)(bool) | Sättare för [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/). |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man skapar en rad för en signatur och infogar den i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_AllowComments(true);
options->set_DefaultInstructions(true);
options->set_Email(u"john.doe@management.com");
options->set_Instructions(u"Please sign here");
options->set_ShowDate(true);
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Senior Manager");

// Infoga en form som kommer att innehålla en signaturrad, vars utseende vi kommer att
// anpassa med hjälp av objektet "SignatureLineOptions" som vi har skapat ovan.
// Om vi infogar en form vars koordinater börjar i sidans nedre högra hörn,
// behöver vi ange negativa x- och y-koordinater för att få formen att visas.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// Verifiera egenskaperna för vår signaturrad via dess Shape-objekt.
System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = shape->get_SignatureLine();

ASSERT_EQ(u"john.doe@management.com", signatureLine->get_Email());
ASSERT_EQ(u"John Doe", signatureLine->get_Signer());
ASSERT_EQ(u"Senior Manager", signatureLine->get_SignerTitle());
ASSERT_EQ(u"Please sign here", signatureLine->get_Instructions());
ASSERT_TRUE(signatureLine->get_ShowDate());
ASSERT_TRUE(signatureLine->get_AllowComments());
ASSERT_TRUE(signatureLine->get_DefaultInstructions());

doc->Save(get_ArtifactsDir() + u"Shape.SignatureLine.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
