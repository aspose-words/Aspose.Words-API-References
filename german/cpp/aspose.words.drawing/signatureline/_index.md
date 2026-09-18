---
title: "Aspose::Words::Drawing::SignatureLine class"
linktitle: "SignatureLine"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::SignatureLine class. Stellt Zugriff auf Eigenschaften der Signaturzeile bereit. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


Stellt Zugriff auf Eigenschaften von Signaturzeilen bereit. Weitere Informationen finden Sie im Dokumentationsartikel [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLine : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | Liest oder legt einen Wert fest, der angibt, dass der Unterzeichner im Signaturdialog Kommentare hinzufügen kann. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() | Liest oder legt einen Wert fest, der angibt, dass die Standardanweisungen im Signaturdialog angezeigt werden. Der Standardwert für diese Eigenschaft ist **true**. |
| [get_Email](./get_email/)() | Liest oder legt die vorgeschlagene E‑Mail‑Adresse des Unterzeichners fest. Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_Id](./get_id/)() | Liefert oder setzt den Bezeichner für diese Signaturzeile. Dieser Bezeichner kann mit einer digitalen Signatur verknüpft werden, wenn das Dokument mit [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/) signiert wird. Dieser Wert muss eindeutig sein und wird standardmäßig zufällig als neue GUID (**NewGuid**) generiert. |
| [get_Instructions](./get_instructions/)() | Liefert oder setzt Anweisungen für den Unterzeichner, die beim Signieren der Signaturzeile angezeigt werden. Diese Eigenschaft wird ignoriert, wenn [DefaultInstructions](./get_defaultinstructions/) gesetzt ist. Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_IsSigned](./get_issigned/)() | Gibt an, dass die Signaturzeile durch eine digitale Signatur unterschrieben ist. |
| [get_IsValid](./get_isvalid/)() | Gibt an, dass die Signaturzeile mit einer digitalen Signatur signiert ist und diese digitale Signatur gültig ist. |
| [get_ProviderId](./get_providerid/)() | Liest oder legt die Kennung des Signaturanbieters für diese Signaturzeile fest. Der Standardwert ist "{00000000-0000-0000-0000-000000000000}". |
| [get_ShowDate](./get_showdate/)() | Liest oder legt einen Wert fest, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. Der Standardwert für diese Eigenschaft ist **true**. |
| [get_Signer](./get_signer/)() | Liest oder legt den vorgeschlagenen Unterzeichner der Signaturzeile fest. Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_SignerTitle](./get_signertitle/)() | Liest oder legt den vorgeschlagenen Titel des Unterzeichners fest (z. B. Manager). Der Standardwert für diese Eigenschaft ist **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Setter für [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Setter für [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Setter für [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/). |
| [set_Id](./set_id/)(System::Guid) | Setter für [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Setter für [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Setter für [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/). |
| [set_ShowDate](./set_showdate/)(bool) | Setter für [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Setter für [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/). |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Setter für [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
