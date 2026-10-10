---
title: "Aspose::Words::DigitalSignatures::CertificateHolder classe"
linktitle: "CertificateHolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder classe. Rappresenta un contenitore di un'istanza X509Certificate2. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


Rappresenta un contenitore di un'istanza **X509Certificate2**. Per saperne di più, visita l'articolo di documentazione [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class CertificateHolder : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | Crea un oggetto [CertificateHolder](./) utilizzando l'array di byte del negozio PKCS12 e la sua password. |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | Crea un oggetto [CertificateHolder](./) utilizzando l'array di byte del negozio PKCS12 e la sua password. |
| static [Create](./create/)(const System::String\&, const System::String\&) | Crea un oggetto [CertificateHolder](./) utilizzando il percorso del negozio PKCS12 e la sua password. |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | Crea un oggetto [CertificateHolder](./) utilizzando il percorso del negozio PKCS12, la sua password e l'alias con cui verranno trovati la chiave privata e il certificato. |
| [get_Certificate](./get_certificate/)() | Restituisce l'istanza di **X509Certificate2** che contiene chiavi private, pubbliche e la catena di certificati. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Note


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

## Esempi



Mostra come firmare digitalmente i documenti.
```cpp
// Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Crea un commento e una data che saranno applicati con la nostra nuova firma digitale.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Prendi un documento non firmato dal file system locale tramite un flusso di file,
// quindi crea una copia firmata determinata dal nome file del flusso di file di output.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```


Mostra come firmare un file di documento crittografato.
```cpp
// Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Crea un commento, una data e una password di decrittazione che saranno applicati con la nostra nuova firma digitale.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Imposta un nome file locale di sistema per il documento di input non firmato e un nome file di output per la sua nuova copia firmata digitalmente.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Vedi anche

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
