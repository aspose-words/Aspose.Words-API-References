---
title: Aspose::Words::DigitalSignatures::CertificateHolder::Create method
linktitle: Create
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::CertificateHolder::Create method. Creates CertificateHolder object using byte array of PKCS12 store and its password in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


Creates [CertificateHolder](../) object using byte array of PKCS12 store and its password.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| Parameter | Type | Description |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | A byte array that contains data from an X.509 certificate. |
| password | const System::SharedPtr\<System::Security::SecureString\>\& | The password required to access the X.509 certificate data. |

### ReturnValue

An instance of [CertificateHolder](../)

## See Also

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


Creates [CertificateHolder](../) object using byte array of PKCS12 store and its password.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| Parameter | Type | Description |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | A byte array that contains data from an X.509 certificate. |
| password | const System::String\& | The password required to access the X.509 certificate data. |

### ReturnValue

An instance of [CertificateHolder](../)

## See Also

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


Creates [CertificateHolder](../) object using path to PKCS12 store and its password.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The name of a certificate file. |
| password | const System::String\& | The password required to access the X.509 certificate data. |

### ReturnValue

An instance of [CertificateHolder](../)

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

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


Creates [CertificateHolder](../) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The name of a certificate file. |
| password | const System::String\& | The password required to access the X.509 certificate data. |
| alias | const System::String\& | The associated alias for a certificate and its private key |

### ReturnValue

An instance of [CertificateHolder](../)

## See Also

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
