---
title: Aspose::Words::DigitalSignatures::SignOptions::set_DecryptionPassword method
linktitle: set_DecryptionPassword
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::SignOptions::set_DecryptionPassword method. The password to decrypt source document. Default value is empty string in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.digitalsignatures/signoptions/set_decryptionpassword/
---
## SignOptions::set_DecryptionPassword method


The password to decrypt source document. Default value is empty string.

```cpp
void Aspose::Words::DigitalSignatures::SignOptions::set_DecryptionPassword(const System::String & value)
```

## Remarks

 If OOXML document is encrypted, you should provide decryption password to decrypt source document before it will be signed. This is not required for documents in binary DOC format. 
## Examples


Shows how to sign encrypted document file.

```cpp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Create a comment, date, and decryption password which will be applied with our new digital signature.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```
## See Also

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
