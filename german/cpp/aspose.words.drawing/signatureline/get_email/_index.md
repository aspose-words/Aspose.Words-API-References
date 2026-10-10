---
title: "Aspose::Words::Drawing::SignatureLine::get_Email Methode"
linktitle: "get_Email"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::SignatureLine::get_Email Methode. Ruft die vorgeschlagene E‑Mail‑Adresse des Unterzeichners ab oder legt sie fest. Der Standardwert für diese Eigenschaft ist eine leere Zeichenkette in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing/signatureline/get_email/
---
## SignatureLine::get_Email method


Liest oder legt die vorgeschlagene E‑Mail‑Adresse des Unterzeichners fest. Der Standardwert für diese Eigenschaft ist **empty string**.

```cpp
System::String Aspose::Words::Drawing::SignatureLine::get_Email()
```


## Beispiele



Zeigt, wie man eine Zeile für eine Signatur erstellt und in ein Dokument einfügt.
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

// Fügen Sie eine Form ein, die eine Signaturzeile enthält, deren Aussehen wir
// mit dem Objekt "SignatureLineOptions" anpassen, das wir oben erstellt haben.
// Wenn wir eine Form einfügen, deren Koordinaten am rechten unteren Eck der Seite beginnen,
// müssen wir negative x- und y-Koordinaten angeben, um die Form sichtbar zu machen.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// Überprüfen Sie die Eigenschaften unserer Signaturzeile über ihr Shape-Objekt.
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

## Siehe auch

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
