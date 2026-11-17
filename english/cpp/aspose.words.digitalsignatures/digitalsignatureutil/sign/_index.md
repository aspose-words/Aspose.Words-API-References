---
title: Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign method
linktitle: Sign
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign method. Signs source document using given CertificateHolder with digital signature and writes signed document to destination stream. Supported formats are: Doc, Dot, Docx, Dotx, Docm, Dotm, Odt, Ott.Output will be written to the start of stream and stream size will be updated with content length in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\> \&, const System::SharedPtr\<System::IO::Stream\> \&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \&) method


Signs source document using given [CertificateHolder](../../certificateholder/) with digital signature and writes signed document to destination stream. 
Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

Output will be written to the start of stream and stream size will be updated with content length.

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> & srcStream, const System::SharedPtr<System::IO::Stream> & dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> & certHolder)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\> \& | The stream which contains the document to sign. |
| dstStream | const System::SharedPtr\<System::IO::Stream\> \& | The stream that signed document will be written to. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |
## Examples


Shows how to sign documents with X.509 certificates.

```cpp
// Verify that a document is not signed.
ASSERT_FALSE(FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Take a document from a stream and save a signed copy to another stream.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Please verify that all of the document's digital signatures are valid and check their details.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"Document.DigitalSignature.docx"));
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(digitalSignatureCollection->get_Count(), 1);
ASSERT_EQ(digitalSignatureCollection->idx_get(0)->get_SignatureType(), DigitalSignatureType::XmlDsig);
ASSERT_EQ(signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName(), u"CN=Morzal.Me");
ASSERT_EQ(signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName(), u"CN=Morzal.Me");
```
## See Also

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\> \&, const System::SharedPtr\<System::IO::Stream\> \&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\> \&) method


Signs source document using given [CertificateHolder](../../certificateholder/) and [SignOptions](../../signoptions/) with digital signature and writes signed document to destination stream. 
Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

Output will be written to the start of stream and stream size will be updated with content length.

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> & srcStream, const System::SharedPtr<System::IO::Stream> & dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> & certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> & signOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\> \& | The stream which contains the document to sign. |
| dstStream | const System::SharedPtr\<System::IO::Stream\> \& | The stream that signed document will be written to. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\> \& | [SignOptions](../../signoptions/) object with various signing options. |
## Examples


Shows how to digitally sign documents.

```cpp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Create a comment and date which will be applied with our new digital signature.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Take an unsigned document from the local file system via a file stream,
// then create a signed copy of it determined by the filename of the output file stream.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```
## See Also

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String \&, const System::String \&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \&) method


Signs source document using given [CertificateHolder](../../certificateholder/) with digital signature and writes signed document to destination file. 
Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String & srcFileName, const System::String & dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> & certHolder)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | const System::String \& | The file name of the document to sign. |
| dstFileName | const System::String \& | The file name of the signed document output. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |
## Examples


Shows how to sign documents with X.509 certificates.

```cpp
// Verify that a document is not signed.
ASSERT_FALSE(FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Take a document from a stream and save a signed copy to another stream.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Please verify that all of the document's digital signatures are valid and check their details.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"Document.DigitalSignature.docx"));
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(digitalSignatureCollection->get_Count(), 1);
ASSERT_EQ(digitalSignatureCollection->idx_get(0)->get_SignatureType(), DigitalSignatureType::XmlDsig);
ASSERT_EQ(signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName(), u"CN=Morzal.Me");
ASSERT_EQ(signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName(), u"CN=Morzal.Me");
```
## See Also

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String \&, const System::String \&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\> \&) method


Signs source document using given [CertificateHolder](../../certificateholder/) and [SignOptions](../../signoptions/) with digital signature and writes signed document to destination file. 
Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String & srcFileName, const System::String & dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> & certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> & signOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | const System::String \& | The file name of the document to sign. |
| dstFileName | const System::String \& | The file name of the signed document output. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\> \& | [SignOptions](../../signoptions/) object with various signing options. |
## Examples


Shows how to sign a document with additional signing options.

```cpp
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_WindowsVersion(u"10.0");
signOptions->set_ApplicationVersion(u"16.0.19127");
signOptions->set_OfficeVersion(u"16.0.19127/27");
signOptions->set_HorizontalResolution(1024);
signOptions->set_VerticalResolution(768);
signOptions->set_ColorDepth(24);

System::ArrayPtr<uint8_t> certBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"morzal.pfx");
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> cert = CertificateHolder::Create(certBytes, u"aw");
DigitalSignatureUtil::Sign(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.docx", cert, signOptions);

auto signedDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"DigitalSignatureUtil.docx"));

System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature> signature = signedDoc->get_DigitalSignatures()->idx_get(0);
ASSERT_EQ(signedDoc->get_DigitalSignatures()->get_Count(), 1);
ASSERT_TRUE(signature->get_IsValid());
ASSERT_EQ(signature->get_WindowsVersion(), u"10.0");
ASSERT_EQ(signature->get_ApplicationVersion(), u"16.0.19127");
ASSERT_EQ(signature->get_OfficeVersion(), u"16.0.19127/27");
ASSERT_EQ(signature->get_HorizontalResolution(), 1024);
ASSERT_EQ(signature->get_VerticalResolution(), 768);
ASSERT_EQ(signature->get_ColorDepth(), 24);
```

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```cpp
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(XmlDsigLevel::XAdEsT);
signOptions->set_TimestampSettings(System::MakeObject<Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings>(u"https://freetsa.org/tsr", u"JohnDoe", u"MyPassword"));

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> cert = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

DigitalSignatureUtil::Sign(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

auto signedDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"DigitalSignatureUtil.Timestamped.docx"));

ASSERT_EQ(signedDoc->get_DigitalSignatures()->get_Count(), 1);
ASSERT_TRUE(signedDoc->get_DigitalSignatures()->idx_get(0)->get_IsValid());

// Verify timestamp settings are applied.
ASSERT_EQ(signOptions->get_TimestampSettings()->get_ServerUrl(), u"https://freetsa.org/tsr");
ASSERT_EQ(signOptions->get_TimestampSettings()->get_UserName(), u"JohnDoe");
ASSERT_EQ(signOptions->get_TimestampSettings()->get_Password(), u"MyPassword");
ASPOSE_ASSERT_EQ(signOptions->get_TimestampSettings()->get_Timeout().get_TotalSeconds(), 100.0);

// Test with custom timeout.
signOptions->set_TimestampSettings(System::MakeObject<Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings>(u"https://freetsa.org/tsr", u"JohnDoe", u"MyPassword", System::TimeSpan::FromMinutes(30)));

ASPOSE_ASSERT_EQ(signOptions->get_TimestampSettings()->get_Timeout().get_TotalSeconds(), 1800.0);
```
## See Also

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\> \&, std::basic_ostream\<CharType, Traits\> \&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \&) method


Signs source document using given [CertificateHolder](../../certificateholder/) with digital signature and writes signed document to destination stream. 
Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

Output will be written to the start of stream and stream size will be updated with content length.

```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> & srcStream, std::basic_ostream<CharType, Traits> & dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> & certHolder)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | std::basic_istream\<CharType, Traits\> \& | The stream which contains the document to sign. |
| dstStream | std::basic_ostream\<CharType, Traits\> \& | The stream that signed document will be written to. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |
## Examples


Shows how to sign documents with X.509 certificates.

```cpp
// Verify that a document is not signed.
ASSERT_FALSE(FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Take a document from a stream and save a signed copy to another stream.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Please verify that all of the document's digital signatures are valid and check their details.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"Document.DigitalSignature.docx"));
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(digitalSignatureCollection->get_Count(), 1);
ASSERT_EQ(digitalSignatureCollection->idx_get(0)->get_SignatureType(), DigitalSignatureType::XmlDsig);
ASSERT_EQ(signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName(), u"CN=Morzal.Me");
ASSERT_EQ(signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName(), u"CN=Morzal.Me");
```
## See Also

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\> \&, std::basic_ostream\<CharType, Traits\> \&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\> \&) method


Signs source document using given [CertificateHolder](../../certificateholder/) and [SignOptions](../../signoptions/) with digital signature and writes signed document to destination stream. 
Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

Output will be written to the start of stream and stream size will be updated with content length.

```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> & srcStream, std::basic_ostream<CharType, Traits> & dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> & certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> & signOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | std::basic_istream\<CharType, Traits\> \& | The stream which contains the document to sign. |
| dstStream | std::basic_ostream\<CharType, Traits\> \& | The stream that signed document will be written to. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\> \& | [SignOptions](../../signoptions/) object with various signing options. |
## Examples


Shows how to digitally sign documents.

```cpp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Create a comment and date which will be applied with our new digital signature.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Take an unsigned document from the local file system via a file stream,
// then create a signed copy of it determined by the filename of the output file stream.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```
## See Also

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
