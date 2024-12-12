---
title: Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign method
linktitle: Sign
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign method. Signs source document using given CertificateHolder with digital signature and writes signed document to destination stream. Supported formats are: Doc, Dot, Docx, Dotx, Docm, Odt, Ott.Output will be written to the start of stream and stream size will be updated with content length in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


Signs source document using given [CertificateHolder](../../certificateholder/) with digital signature and writes signed document to destination stream. Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).**Output will be written to the start of stream and stream size will be updated with content length.**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | The stream which contains the document to sign. |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | The stream that signed document will be written to. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |

## Examples



Shows how to sign documents with X.509 certificates. 
```cpp
// Verify that a document is not signed.
ASSERT_FALSE(FileFormatUtil::DetectFileFormat(MyDir + u"Document.docx")->get_HasDigitalSignature());

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw", nullptr);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
auto signOptions = MakeObject<SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());

DigitalSignatureUtil::Sign(MyDir + u"Document.docx", ArtifactsDir + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(ArtifactsDir + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Take a document from a stream and save a signed copy to another stream.
{
    auto inDoc = MakeObject<System::IO::FileStream>(MyDir + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = MakeObject<System::IO::FileStream>(ArtifactsDir + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(ArtifactsDir + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Please verify that all of the document's digital signatures are valid and check their details.
auto signedDoc = MakeObject<Document>(ArtifactsDir + u"Document.DigitalSignature.docx");
SharedPtr<DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## See Also

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


Signs source document using given [CertificateHolder](../../certificateholder/) and [SignOptions](../../signoptions/) with digital signature and writes signed document to destination stream. Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).**Output will be written to the start of stream and stream size will be updated with content length.**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | The stream which contains the document to sign. |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | The stream that signed document will be written to. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | [SignOptions](../../signoptions/) object with various signing options. |

## Examples



Shows how to digitally sign documents. 
```cpp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw");

// Create a comment and date which will be applied with our new digital signature.
auto signOptions = MakeObject<SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Take an unsigned document from the local file system via a file stream,
// then create a signed copy of it determined by the filename of the output file stream.
{
    SharedPtr<System::IO::Stream> streamIn = MakeObject<System::IO::FileStream>(MyDir + u"Document.docx", System::IO::FileMode::Open);
    {
        SharedPtr<System::IO::Stream> streamOut =
            MakeObject<System::IO::FileStream>(ArtifactsDir + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## See Also

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


Signs source document using given [CertificateHolder](../../certificateholder/) with digital signature and writes signed document to destination file. Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | const System::String\& | The file name of the document to sign. |
| dstFileName | const System::String\& | The file name of the signed document output. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |

## Examples



Shows how to sign documents with X.509 certificates. 
```cpp
// Verify that a document is not signed.
ASSERT_FALSE(FileFormatUtil::DetectFileFormat(MyDir + u"Document.docx")->get_HasDigitalSignature());

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw", nullptr);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
auto signOptions = MakeObject<SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());

DigitalSignatureUtil::Sign(MyDir + u"Document.docx", ArtifactsDir + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(ArtifactsDir + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Take a document from a stream and save a signed copy to another stream.
{
    auto inDoc = MakeObject<System::IO::FileStream>(MyDir + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = MakeObject<System::IO::FileStream>(ArtifactsDir + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(ArtifactsDir + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Please verify that all of the document's digital signatures are valid and check their details.
auto signedDoc = MakeObject<Document>(ArtifactsDir + u"Document.DigitalSignature.docx");
SharedPtr<DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## See Also

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


Signs source document using given [CertificateHolder](../../certificateholder/) and [SignOptions](../../signoptions/) with digital signature and writes signed document to destination file. Supported formats are: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | const System::String\& | The file name of the document to sign. |
| dstFileName | const System::String\& | The file name of the signed document output. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | [SignOptions](../../signoptions/) object with various signing options. |

## Examples



Shows how to add a signature line to a document, and then sign it using a digital certificate. 
```cpp
static void Sign()
{
    String signeeName = u"Ron Williams";
    String srcDocumentPath = MyDir + u"Document.docx";
    String dstDocumentPath = ArtifactsDir + u"SignDocumentCustom.Sign.docx";
    String certificatePath = MyDir + u"morzal.pfx";
    String certificatePassword = u"aw";

    CreateSignees();

    auto signeeInfo = mSignees->Find(System::Predicate<SharedPtr<Signee>>([&](SharedPtr<Signee> c) { return c->get_Name() == signeeName; }));

    if (signeeInfo != nullptr)
    {
        SignDocument(srcDocumentPath, dstDocumentPath, signeeInfo, certificatePath, certificatePassword);
    }
    else
    {
        FAIL() << "Signee does not exist.";
    }
}

class Signee : public System::Object
{
public:
    System::Guid get_PersonId()
    {
        return pr_PersonId;
    }

    void set_PersonId(System::Guid value)
    {
        pr_PersonId = value;
    }

    String get_Name()
    {
        return pr_Name;
    }

    void set_Name(String value)
    {
        pr_Name = value;
    }

    String get_Position()
    {
        return pr_Position;
    }

    void set_Position(String value)
    {
        pr_Position = value;
    }

    ArrayPtr<uint8_t> get_Image()
    {
        return pr_Image;
    }

    void set_Image(ArrayPtr<uint8_t> value)
    {
        pr_Image = value;
    }

    Signee(System::Guid guid, String name, String position, ArrayPtr<uint8_t> image)
    {
        set_PersonId(guid);
        set_Name(name);
        set_Position(position);
        set_Image(image);
    }

private:
    System::Guid pr_PersonId;
    String pr_Name;
    String pr_Position;
    ArrayPtr<uint8_t> pr_Image;
};
static void SignDocument(String srcDocumentPath, String dstDocumentPath, SharedPtr<ExSignDocumentCustom::Signee> signeeInfo, String certificatePath,
                         String certificatePassword)
{
    auto document = MakeObject<Document>(srcDocumentPath);
    auto builder = MakeObject<DocumentBuilder>(document);

    // Configure and insert a signature line, an object in the document that will display a signature that we sign it with.
    auto signatureLineOptions = MakeObject<SignatureLineOptions>();
    signatureLineOptions->set_Signer(signeeInfo->get_Name());
    signatureLineOptions->set_SignerTitle(signeeInfo->get_Position());

    SharedPtr<SignatureLine> signatureLine = builder->InsertSignatureLine(signatureLineOptions)->get_SignatureLine();
    signatureLine->set_Id(signeeInfo->get_PersonId());

    // First, we will save an unsigned version of our document.
    builder->get_Document()->Save(dstDocumentPath);

    SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(certificatePath, certificatePassword);

    auto signOptions = MakeObject<SignOptions>();
    signOptions->set_SignatureLineId(signeeInfo->get_PersonId());
    signOptions->set_SignatureLineImage(signeeInfo->get_Image());

    // Overwrite the unsigned document we saved above with a version signed using the certificate.
    DigitalSignatureUtil::Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
}

static ArrayPtr<uint8_t> ImageToByteArray(SharedPtr<System::Drawing::Image> imageIn)
{
    {
        auto ms = MakeObject<System::IO::MemoryStream>();
        imageIn->Save(ms, System::Drawing::Imaging::ImageFormat::get_Png());
        return ms->ToArray();
    }
}

static void CreateSignees()
{
    mSignees = MakeObject<System::Collections::Generic::List<SharedPtr<ExSignDocumentCustom::Signee>>>();
    mSignees->Add(MakeObject<ExSignDocumentCustom::Signee>(System::Guid::NewGuid(), u"Ron Williams", u"Chief Executive Officer",
                                                           ImageToByteArray(System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg"))));
    mSignees->Add(MakeObject<ExSignDocumentCustom::Signee>(System::Guid::NewGuid(), u"Stephen Morse", u"Head of Compliance",
                                                           ImageToByteArray(System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg"))));
}

static SharedPtr<System::Collections::Generic::List<SharedPtr<ExSignDocumentCustom::Signee>>> mSignees;
```

## See Also

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder)
```

## See Also

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder, System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> signOptions)
```

## See Also

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
