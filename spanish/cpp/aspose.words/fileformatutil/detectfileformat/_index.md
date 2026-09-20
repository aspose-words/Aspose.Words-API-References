---
title: "Método Aspose::Words::FileFormatUtil::DetectFileFormat"
linktitle: "DetectFileFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::FileFormatUtil::DetectFileFormat. Detecta y devuelve la información sobre el formato de un documento almacenado en un flujo en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


Detecta y devuelve la información sobre el formato de un documento almacenado en un flujo.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | El flujo. |

### ReturnValue

Un objeto [FileFormatInfo](../../fileformatinfo/) que contiene la información detectada.
## Observaciones


El flujo debe estar posicionado al comienzo del documento.

Cuando este método devuelve, la posición del flujo se restaura a la posición original.

Aunque este método detecte el formato del documento, no garantiza que el documento especificado sea válido. Este método solo detecta el formato del documento leyendo datos que son suficientes para la detección. Para verificar completamente que un documento sea válido, es necesario cargar el documento en un objeto [Document](../../document/).

Este método lanza [FileCorruptedException](../../filecorruptedexception/) cuando se reconoce el formato, pero la detección no puede completarse debido a la corrupción.

## Ejemplos



Muestra cómo usar los métodos de [FileFormatUtil](../) para detectar el formato de un documento.
```cpp
// Cargue un documento desde un archivo que no tiene extensión y luego detecte su formato de archivo.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // A continuación se presentan dos métodos para convertir un LoadFormat a su SaveFormat correspondiente.
    // 1 - Obtenga la cadena de extensión de archivo para el LoadFormat y luego obtenga el SaveFormat correspondiente a partir de esa cadena:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 - Convierta directamente el LoadFormat a su SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Cargue un documento desde el flujo y luego guárdelo con la extensión de archivo detectada automáticamente.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## Ver también

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


Detecta y devuelve la información sobre el formato de un documento almacenado en un archivo en disco.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El nombre del archivo. |

### ReturnValue

Un objeto [FileFormatInfo](../../fileformatinfo/) que contiene la información detectada.
## Observaciones


Aunque este método detecte el formato del documento, no garantiza que el documento especificado sea válido. Este método solo detecta el formato del documento leyendo datos que son suficientes para la detección. Para verificar completamente que un documento sea válido, es necesario cargar el documento en un objeto [Document](../../document/).

Este método lanza [FileCorruptedException](../../filecorruptedexception/) cuando se reconoce el formato, pero la detección no puede completarse debido a la corrupción.

## Ejemplos



Muestra cómo usar la clase [FileFormatUtil](../) para detectar el formato del documento y el cifrado.
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


Muestra cómo usar la clase [FileFormatUtil](../) para detectar el formato del documento y la presencia de firmas digitales.
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

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## Ver también

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
