---
title: "Método Sign de Aspose::Words::DigitalSignatures::DigitalSignatureUtil"
linktitle: "Sign"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Sign de Aspose::Words::DigitalSignatures::DigitalSignatureUtil. Firma el documento de origen usando el CertificateHolder proporcionado con firma digital y escribe el documento firmado en el flujo de destino. Los formatos compatibles son: Doc, Dot, Docx, Dotx, Docm, Dotm, Odt, Ott. La salida se escribirá al inicio del flujo y el tamaño del flujo se actualizará con la longitud del contenido en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


Firma el documento de origen usando el [CertificateHolder](../../certificateholder/) proporcionado con firma digital y escribe el documento firmado en el flujo de destino. Los formatos compatibles son: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).**La salida se escribirá al inicio del flujo y el tamaño del flujo se actualizará con la longitud del contenido.**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo que contiene el documento a firmar. |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo en el que se escribirá el documento firmado. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | Objeto [CertificateHolder](../../certificateholder/) con el certificado que se utilizó para firmar el archivo. El certificado en el holder DEBE contener claves privadas. |

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

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


Firma el documento de origen usando el [CertificateHolder](../../certificateholder/) y [SignOptions](../../signoptions/) proporcionados con firma digital y escribe el documento firmado en el flujo de destino. Los formatos compatibles son: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).**La salida se escribirá al inicio del flujo y el tamaño del flujo se actualizará con la longitud del contenido.**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo que contiene el documento a firmar. |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo en el que se escribirá el documento firmado. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | Objeto [CertificateHolder](../../certificateholder/) con el certificado que se utilizó para firmar el archivo. El certificado en el holder DEBE contener claves privadas. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | Objeto [SignOptions](../../signoptions/) con varias opciones de firma. |

## Ejemplos



Muestra cómo firmar digitalmente documentos.
```cpp
// Crea un certificado X.509 a partir de un almacén PKCS#12, que debe contener una clave privada.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Crea un comentario y una fecha que se aplicarán con nuestra nueva firma digital.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Obtén un documento sin firmar del sistema de archivos local mediante un flujo de archivo,
// luego crea una copia firmada del mismo determinada por el nombre de archivo del flujo de salida.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Ver también

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


Firma el documento de origen usando el [CertificateHolder](../../certificateholder/) con firma digital y escribe el documento firmado en el archivo de destino. Los formatos compatibles son: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcFileName | const System::String\& | El nombre de archivo del documento a firmar. |
| dstFileName | const System::String\& | El nombre de archivo del documento firmado de salida. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | Objeto [CertificateHolder](../../certificateholder/) con el certificado que se utilizó para firmar el archivo. El certificado en el holder DEBE contener claves privadas. |

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

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


Firma el documento de origen usando el [CertificateHolder](../../certificateholder/) y [SignOptions](../../signoptions/) con firma digital y escribe el documento firmado en el archivo de destino. Los formatos compatibles son: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcFileName | const System::String\& | El nombre de archivo del documento a firmar. |
| dstFileName | const System::String\& | El nombre de archivo del documento firmado de salida. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | Objeto [CertificateHolder](../../certificateholder/) con el certificado que se utilizó para firmar el archivo. El certificado en el holder DEBE contener claves privadas. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | Objeto [SignOptions](../../signoptions/) con varias opciones de firma. |

## Ejemplos



Muestra cómo firmar un documento con opciones de firma adicionales.
```cpp
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_WindowsVersion(u"10.0");
signOptions->set_ApplicationVersion(u"16.0.19127");
signOptions->set_OfficeVersion(u"16.0.19127/27");
signOptions->set_HorizontalResolution(1024);
signOptions->set_VerticalResolution(768);
signOptions->set_ColorDepth(24);

System::ArrayPtr<uint8_t> certBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"morzal.pfx");
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> cert = Aspose::Words::DigitalSignatures::CertificateHolder::Create(certBytes, u"aw");
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.docx", cert, signOptions);

auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DigitalSignatureUtil.docx");

System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature> signature = signedDoc->get_DigitalSignatures()->idx_get(0);
ASSERT_EQ(1, signedDoc->get_DigitalSignatures()->get_Count());
ASSERT_TRUE(signature->get_IsValid());
ASSERT_EQ(u"10.0", signature->get_WindowsVersion());
ASSERT_EQ(u"16.0.19127", signature->get_ApplicationVersion());
ASSERT_EQ(u"16.0.19127/27", signature->get_OfficeVersion());
ASSERT_EQ(1024, signature->get_HorizontalResolution());
ASSERT_EQ(768, signature->get_VerticalResolution());
ASSERT_EQ(24, signature->get_ColorDepth());
```

## Ver también

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder)
```

## Ver también

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder, System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> signOptions)
```

## Ver también

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
