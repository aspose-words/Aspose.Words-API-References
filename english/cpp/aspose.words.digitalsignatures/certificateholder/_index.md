---
title: CertificateHolder
second_title: Aspose.Words for C++ API Reference
description: Represents a holder of X509Certificate2 instance. To learn more, visit the  documentation article.
type: docs
weight: 1
url: /cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


Represents a holder of **X509Certificate2** instance. To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) documentation article.

```cpp
class CertificateHolder : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | Creates [CertificateHolder](./) object using byte array of PKCS12 store and its password. |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | Creates [CertificateHolder](./) object using byte array of PKCS12 store and its password. |
| static [Create](./create/)(const System::String\&, const System::String\&) | Creates [CertificateHolder](./) object using path to PKCS12 store and its password. |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | Creates [CertificateHolder](./) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found. |
| [get_Certificate](./get_certificate/)() | Returns the instance of **X509Certificate2** which holds private, public keys and certificate chain. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarks


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

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


Shows how to sign encrypted document file. 
```cpp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw");

// Create a comment, date, and decryption password which will be applied with our new digital signature.
auto signOptions = MakeObject<SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
String inputFileName = MyDir + u"Encrypted.docx";
String outputFileName = ArtifactsDir + u"DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```


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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words](../../)
