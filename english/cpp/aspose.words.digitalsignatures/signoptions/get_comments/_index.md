---
title: get_Comments
second_title: Aspose.Words for C++ API Reference
description: Specifies comments on the digital signature. Default value is empty string.
type: docs
weight: 14
url: /cpp/aspose.words.digitalsignatures/signoptions/get_comments/
---
## SignOptions.get_Comments method


Specifies comments on the digital signature. Default value is **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_Comments() const
```


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

