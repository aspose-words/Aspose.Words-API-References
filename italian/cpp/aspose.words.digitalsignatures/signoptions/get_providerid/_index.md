---
title: "metodo Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId"
linktitle: "get_ProviderId"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId. Specifica l'ID di classe del provider di firma. Il valore predefinito è Empty (tutti zero) Guid in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.digitalsignatures/signoptions/get_providerid/
---
## SignOptions::get_ProviderId method


Specifica l'ID classe del provider di firma. Il valore predefinito è **Empty (all zeroes) Guid**.

```cpp
System::Guid Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId() const
```

## Note


Il provider di servizi crittografici (CSP) è un modulo software indipendente che esegue effettivamente gli algoritmi di crittografia per l'autenticazione, la codifica e la cifratura. MS Office riserva il valore {00000000-0000-0000-0000-000000000000} per il suo provider di firma predefinito.

Il GUID del provider aggiuntivamente installato dovrebbe essere ottenuto dalla documentazione fornita con il provider.

Inoltre, tutti i provider crittografici installati sono elencati nel registro di Windows. È possibile trovarli nel seguente percorso: HKLM\SOFTWARE\**Microsoft**\Cryptography\Defaults\Provider. Esiste una chiave denominata "CP Service UUID" che corrisponde a un GUID del provider di firma.

## Esempi



Mostra come firmare un documento con un certificato personale e una riga della firma.
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

// Riapri il nostro documento salvato e verifica che le proprietà "IsSigned" e "IsValid" siano entrambe uguali a "true",
// indicando che la riga della firma contiene una firma.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## Vedi anche

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
