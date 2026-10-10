---
title: "Aspose::Words::Drawing::SignatureLine::get_Email‑metod"
linktitle: "get_Email"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::SignatureLine::get_Email metod. Hämtar eller anger föreslagen signerares e‑postadress. Standardvärdet för denna egenskap är en tom sträng i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.drawing/signatureline/get_email/
---
## SignatureLine::get_Email method


Hämtar eller anger föreslagen undertecknares e‑postadress. Standardvärdet för denna egenskap är **empty string**.

```cpp
System::String Aspose::Words::Drawing::SignatureLine::get_Email()
```


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

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
