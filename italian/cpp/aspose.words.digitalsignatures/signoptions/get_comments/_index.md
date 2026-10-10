---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_Comments metodo"
linktitle: "get_Comments"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_Comments metodo. Specifica i commenti sulla firma digitale. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.digitalsignatures/signoptions/get_comments/
---
## SignOptions::get_Comments method


Specifica i commenti sulla firma digitale. Il valore predefinito è **stringa vuota**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_Comments() const
```


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

## Vedi anche

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
