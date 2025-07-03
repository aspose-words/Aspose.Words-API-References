---
title: Aspose::Words::DigitalSignatures::CertificateHolder class
linktitle: CertificateHolder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::CertificateHolder class. Represents a holder of X509Certificate2 instance. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
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
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

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
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```


Shows how to sign encrypted document file. 
```cpp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Create a comment, date, and decryption password which will be applied with our new digital signature.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## See Also

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
