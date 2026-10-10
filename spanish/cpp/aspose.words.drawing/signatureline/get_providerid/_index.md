---
title: "Aspose::Words::Drawing::SignatureLine::get_ProviderId método"
linktitle: "get_ProviderId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::SignatureLine::get_ProviderId método. Obtiene o establece el identificador del proveedor de firma para esta línea de firma. El valor predeterminado es \"{00000000-0000-0000-0000-000000000000}\" en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.drawing/signatureline/get_providerid/
---
## SignatureLine::get_ProviderId method


Obtiene o establece el identificador del proveedor de firma para esta línea de firma. El valor predeterminado es "{00000000-0000-0000-0000-000000000000}".

```cpp
System::Guid Aspose::Words::Drawing::SignatureLine::get_ProviderId()
```

## Observaciones


El proveedor de servicios criptográficos (CSP) es un módulo de software independiente que realmente ejecuta algoritmos de criptografía para autenticación, codificación y cifrado. MS Office reserva el valor {00000000-0000-0000-0000-000000000000} para su proveedor de firma predeterminado.

El GUID del proveedor adicionalmente instalado debe obtenerse de la documentación suministrada con el proveedor.

Además, todos los proveedores criptográficos instalados se enumeran en el registro de Windows. Se puede encontrar en la siguiente ruta: HKLM\\SOFTWARE\\**Microsoft**\\Cryptography\\Defaults\\Provider. Existe una clave llamada "CP Service UUID" que corresponde a un GUID del proveedor de firma.

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

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
