---
title: "Aspose::Words::SignatureLineOptions class"
linktitle: "SignatureLineOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::SignatureLineOptions class. Consente di specificare le opzioni per la linea di firma inserita. Utilizzato in DocumentBuilder. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 61000
url: /it/cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


Consente di specificare le opzioni per la linea di firma inserita. Utilizzato in [DocumentBuilder](../documentbuilder/). Per saperne di più, visita l'articolo di documentazione [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLineOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | Ottiene o imposta un valore che indica se il firmatario può aggiungere commenti nella finestra di dialogo di firma. Il valore predefinito per questa proprietà è **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | Ottiene o imposta un valore che indica se le istruzioni predefinite sono visualizzate nella finestra di dialogo Firma. Il valore predefinito per questa proprietà è **true**. |
| [get_Email](./get_email/)() const | Ottiene o imposta l'indirizzo e‑mail del firmatario suggerito. Il valore predefinito per questa proprietà è **empty string**. |
| [get_Instructions](./get_instructions/)() const | Ottiene o imposta le istruzioni per il firmatario visualizzate durante la firma della riga della firma. Il valore predefinito per questa proprietà è **empty string**. |
| [get_ShowDate](./get_showdate/)() const | Ottiene o imposta un valore che indica se la data di firma è visualizzata nella riga della firma. Il valore predefinito per questa proprietà è **true**. |
| [get_Signer](./get_signer/)() const | Ottiene il firmatario suggerito per la riga della firma. Il valore predefinito per questa proprietà è **empty string**. |
| [get_SignerTitle](./get_signertitle/)() const | Ottiene il titolo del firmatario suggerito. Il valore predefinito per questa proprietà è **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Metodo set per [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Metodo set per [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Metodo set per [Aspose::Words::SignatureLineOptions::get_Email](./get_email/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Metodo set per [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/). |
| [set_ShowDate](./set_showdate/)(bool) | Metodo set per [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Imposta il firmatario suggerito per la riga della firma. Il valore predefinito per questa proprietà è **empty string**. |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Imposta il titolo del firmatario suggerito. Il valore predefinito per questa proprietà è **empty string**. |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
