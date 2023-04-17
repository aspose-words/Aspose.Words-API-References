---
title: Aspose::Words::Loading::LoadOptions::get_Password method
linktitle: get_Password
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::get_Password method. Gets or sets the password for opening an encrypted document. Can be null or empty string. Default is null in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


Gets or sets the password for opening an encrypted document. Can be **null** or empty string. Default is **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## Remarks


You need to know the password to open an encrypted document. If the document is not encrypted, set this to **null** or empty string.

## Examples



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

## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
