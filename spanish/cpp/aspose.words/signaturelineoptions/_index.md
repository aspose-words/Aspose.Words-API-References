---
title: "Aspose::Words::SignatureLineOptions class"
linktitle: "SignatureLineOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::SignatureLineOptions class. Permite especificar opciones para la línea de firma que se inserta. Se usa en DocumentBuilder. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 61000
url: /es/cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


Permite especificar opciones para la línea de firma que se inserta. Se usa en [DocumentBuilder](../documentbuilder/). Para obtener más información, visite el artículo de documentación [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLineOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | Obtiene o establece un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo Sign. El valor predeterminado para esta propiedad es **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | Obtiene o establece un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Sign. El valor predeterminado para esta propiedad es **true**. |
| [get_Email](./get_email/)() const | Obtiene o establece la dirección de correo electrónico sugerida del firmante. El valor predeterminado para esta propiedad es **empty string**. |
| [get_Instructions](./get_instructions/)() const | Obtiene o establece las instrucciones para el firmante que se muestran al firmar la línea de firma. El valor predeterminado para esta propiedad es **empty string**. |
| [get_ShowDate](./get_showdate/)() const | Obtiene o establece un valor que indica que la fecha de firma se muestra en la línea de firma. El valor predeterminado para esta propiedad es **true**. |
| [get_Signer](./get_signer/)() const | Obtiene el firmante sugerido de la línea de firma. El valor predeterminado para esta propiedad es **empty string**. |
| [get_SignerTitle](./get_signertitle/)() const | Obtiene el título sugerido del firmante. El valor predeterminado para esta propiedad es **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Método set para [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Método set para [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Método set para [Aspose::Words::SignatureLineOptions::get_Email](./get_email/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Método set para [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/). |
| [set_ShowDate](./set_showdate/)(bool) | Método set para [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Establece el firmante sugerido de la línea de firma. El valor predeterminado para esta propiedad es **empty string**. |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Establece el título sugerido del firmante. El valor predeterminado para esta propiedad es **empty string**. |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo firmar un documento con un certificado personal y una línea de firma.
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

// Vuelva a abrir nuestro documento guardado y verifique que las propiedades "IsSigned" y "IsValid" ambas sean "true",
// indicando que la línea de firma contiene una firma.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
