---
title: get_DecryptionPassword
second_title: Aspose.Words for C++ API Reference
description: The password to decrypt source document. Default value is empty string.
type: docs
weight: 40
url: /cpp/aspose.words.digitalsignatures/signoptions/get_decryptionpassword/
---
## SignOptions::get_DecryptionPassword method


The password to decrypt source document. Default value is **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword() const
```


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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words](../../../)
