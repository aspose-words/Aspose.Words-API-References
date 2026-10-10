---
title: "Aspose::Words::SignatureLineOptions class"
linktitle: "SignatureLineOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::SignatureLineOptions Klasse. Ermöglicht das Festlegen von Optionen für die einzufügende Signaturzeile. Wird in DocumentBuilder verwendet. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 61000
url: /de/cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


Ermöglicht das Festlegen von Optionen für die einzufügende Signaturzeile. Wird in [DocumentBuilder](../documentbuilder/) verwendet. Weitere Informationen finden Sie im Dokumentationsartikel [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLineOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | Liest oder legt einen Wert fest, der angibt, dass der Unterzeichner im Signaturdialog Kommentare hinzufügen kann. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | Liest oder legt einen Wert fest, der angibt, dass die Standardanweisungen im Signaturdialog angezeigt werden. Der Standardwert für diese Eigenschaft ist **true**. |
| [get_Email](./get_email/)() const | Liest oder legt die vorgeschlagene E‑Mail‑Adresse des Unterzeichners fest. Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_Instructions](./get_instructions/)() const | Liest oder legt Anweisungen für den Unterzeichner fest, die beim Signieren der Signaturzeile angezeigt werden. Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_ShowDate](./get_showdate/)() const | Liest oder legt einen Wert fest, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. Der Standardwert für diese Eigenschaft ist **true**. |
| [get_Signer](./get_signer/)() const | Liest den vorgeschlagenen Unterzeichner der Signaturzeile. Der Standardwert für diese Eigenschaft ist **empty string**. |
| [get_SignerTitle](./get_signertitle/)() const | Liest den vorgeschlagenen Titel des Unterzeichners. Der Standardwert für diese Eigenschaft ist **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Setter für [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Setter für [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Setter für [Aspose::Words::SignatureLineOptions::get_Email](./get_email/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Setter für [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/). |
| [set_ShowDate](./set_showdate/)(bool) | Setter für [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Legt den vorgeschlagenen Unterzeichner der Signaturzeile fest. Der Standardwert für diese Eigenschaft ist **empty string**. |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Legt den vorgeschlagenen Titel des Unterzeichners fest. Der Standardwert für diese Eigenschaft ist **empty string**. |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto signatureLineOptions = System::MakeObject<Aspose::Words::SignatureLineOptions>();
signatureLineOptions->set_Signer(u"vderyushev");
signatureLineOptions->set_SignerTitle(u"QA");
signatureLineOptions->set_Email(u"vderyushev@aspose.com");
signatureLineOptions->set_ShowDate(true);
signatureLineOptions->set_DefaultInstructions(false);
signatureLineOptions->set_Instructions(u"Please sign here.");
signatureLineOptions->set_AllowComments(true);

System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = builder->InsertSignatureLine(signatureLineOptions)->get_SignatureLine();
signatureLine->set_ProviderId(System::Guid::Parse(u"CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

ASSERT_FALSE(signatureLine->get_IsSigned());
ASSERT_FALSE(signatureLine->get_IsValid());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignatureLineId(signatureLine->get_Id());
signOptions->set_ProviderId(signatureLine->get_ProviderId());
signOptions->set_Comments(u"Document was signed by vderyushev");
signOptions->set_SignTime(System::DateTime::get_Now());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx", get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Öffnen Sie unser gespeichertes Dokument erneut und prüfen Sie, dass die Eigenschaften "IsSigned" und "IsValid" beide den Wert "true" haben,
// was darauf hinweist, dass die Signaturzeile eine Signatur enthält.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
