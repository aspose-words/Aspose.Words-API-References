---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId Methode"
linktitle: "get_ProviderId"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId Methode. Gibt die Klassen-ID des Signaturproviders an. Der Standardwert ist Empty (alle Nullen) Guid in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.digitalsignatures/signoptions/get_providerid/
---
## SignOptions::get_ProviderId method


Gibt die Klassen-ID des Signaturanbieters an. Standardwert ist **Empty (all zeroes) Guid**.

```cpp
System::Guid Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId() const
```

## Hinweise


Der kryptografische Dienstanbieter (CSP) ist ein unabhängiges Softwaremodul, das tatsächlich Kryptografie‑Algorithmen für Authentifizierung, Codierung und Verschlüsselung ausführt. MS Office reserviert den Wert {00000000-0000-0000-0000-000000000000} für seinen Standard‑Signaturanbieter.

Die GUID des zusätzlich installierten Anbieters sollte aus der mit dem Anbieter gelieferten Dokumentation entnommen werden.

Zusätzlich werden alle installierten kryptografischen Anbieter im Windows‑Registrierungseditor aufgelistet. Sie finden ihn im folgenden Pfad: HKLM\\SOFTWARE\\**Microsoft**\\Cryptography\\Defaults\\Provider. Es gibt einen Schlüsselnamen "CP Service UUID", der einer GUID des Signaturanbieters entspricht.

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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
