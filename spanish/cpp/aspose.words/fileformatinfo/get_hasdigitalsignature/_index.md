---
title: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature método"
linktitle: "get_HasDigitalSignature"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature método. Devuelve true si este documento contiene una firma digital. Esta propiedad simplemente indica que una firma digital está presente en un documento, pero no especifica si la firma es válida o no en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo::get_HasDigitalSignature method


Devuelve **true** si este documento contiene una firma digital. Esta propiedad simplemente indica que una firma digital está presente en un documento, pero no especifica si la firma es válida o no.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```

## Observaciones


Esta propiedad existe para ayudarle a separar los documentos que están firmados digitalmente de los que no lo están. Si utiliza Aspose.Words para modificar y guardar un documento que está firmado digitalmente, la firma digital se perderá. Esto es intencional porque una firma digital sirve para proteger la autenticidad de un documento. Usando esta propiedad puede detectar documentos firmados digitalmente antes de procesarlos de la misma manera que los documentos normales y tomar alguna acción para evitar perder la firma digital, por ejemplo notificar al usuario.

## Ejemplos



Muestra cómo usar la clase [FileFormatUtil](../../fileformatutil/) para detectar el formato del documento y la presencia de firmas digitales.
```cpp
// Utilice una instancia de FileFormatInfo para verificar que un documento no esté firmado digitalmente.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Utilice una nueva instancia de FileFormatInstance para confirmar que está firmado.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// Podemos cargar y acceder a las firmas de un documento firmado en una colección como esta.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## Ver también

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
