---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword metodo"
linktitle: "get_DecryptionPassword"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword metodo. La password per decrittare il documento di origine. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.digitalsignatures/signoptions/get_decryptionpassword/
---
## SignOptions::get_DecryptionPassword method


La password per decrittare il documento di origine. Il valore predefinito è **stringa vuota**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword() const
```


## Esempi



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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
