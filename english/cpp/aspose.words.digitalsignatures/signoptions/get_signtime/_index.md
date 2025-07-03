---
title: Aspose::Words::DigitalSignatures::SignOptions::get_SignTime method
linktitle: get_SignTime
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::SignOptions::get_SignTime method. The date of signing. Default value is current time (Now) in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.digitalsignatures/signoptions/get_signtime/
---
## SignOptions::get_SignTime method


The date of signing. Default value is **current time** (**Now**)

```cpp
System::DateTime Aspose::Words::DigitalSignatures::SignOptions::get_SignTime() const
```


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

## See Also

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
