---
title: "Aspose::Words::FileFormatInfo clase"
linktitle: "FileFormatInfo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FileFormatInfo clase. Contiene datos devueltos por los métodos de detección de formato de documento de FileFormatUtil. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


Contiene datos devueltos por los métodos de detección de formato de documento de [FileFormatUtil](../fileformatutil/). Para obtener más información, visite el artículo de documentación [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatInfo : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | Obtiene la codificación detectada si es aplicable al formato del documento actual. En este momento solo detecta la codificación para documentos HTML. |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | Devuelve **true** si este documento contiene una firma digital. Esta propiedad simplemente indica que una firma digital está presente en un documento, pero no especifica si la firma es válida o no. |
| [get_HasMacros](./get_hasmacros/)() const | Devuelve **true** si este documento contiene macros VBA. |
| [get_IsEncrypted](./get_isencrypted/)() const | Devuelve **true** si el documento está encriptado y requiere una contraseña para abrirse. |
| [get_LoadFormat](./get_loadformat/)() const | Obtiene el formato de documento detectado. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Observaciones


No crea instancias de esta clase directamente. Los objetos de esta clase son devueltos por los métodos [DetectFileFormat()](../).

## Ejemplos



Muestra cómo usar la clase [FileFormatUtil](../fileformatutil/) para detectar el formato del documento y la encriptación.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Configure un objeto SaveOptions para encriptar el documento
// con una contraseña al guardarlo, y luego guarde el documento.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Verifique el tipo de archivo de nuestro documento y su estado de encriptación.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


Muestra cómo usar la clase [FileFormatUtil](../fileformatutil/) para detectar el formato del documento y la presencia de firmas digitales.
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
