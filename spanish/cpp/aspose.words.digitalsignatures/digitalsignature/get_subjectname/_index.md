---
title: "Método get_SubjectName de Aspose::Words::DigitalSignatures::DigitalSignature"
linktitle: "get_SubjectName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_SubjectName de Aspose::Words::DigitalSignatures::DigitalSignature. Devuelve el nombre distinguido del sujeto del certificado que se utilizó para firmar el documento en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.digitalsignatures/digitalsignature/get_subjectname/
---
## DigitalSignature::get_SubjectName method


Devuelve el nombre distinguido del sujeto del certificado que se utilizó para firmar el documento.

```cpp
System::String Aspose::Words::DigitalSignatures::DigitalSignature::get_SubjectName()
```


## Ejemplos



Muestra cómo firmar documentos con certificados X.509.
```cpp
// Verifique que un documento no esté firmado.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Cree un objeto CertificateHolder a partir de un archivo PKCS12, que utilizaremos para firmar el documento.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// Hay dos formas de guardar una copia firmada de un documento en el sistema de archivos local:
// 1 - Designe un documento mediante un nombre de archivo del sistema local y guarde una copia firmada en una ubicación especificada por otro nombre de archivo.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Obtenga un documento de un flujo y guarde una copia firmada en otro flujo.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Por favor, verifique que todas las firmas digitales del documento sean válidas y revise sus detalles.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## Ver también

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
