---
title: "Aspose::Words::Loading::LoadOptions::get_Password metodo"
linktitle: "get_Password"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_Password metodo. Ottiene o imposta la password per aprire un documento crittografato. Può essere null o stringa vuota. Il valore predefinito è null in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


Ottiene o imposta la password per aprire un documento crittografato. Può essere **null** o una stringa vuota. Il valore predefinito è **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## Note


È necessario conoscere la password per aprire un documento crittografato. Se il documento non è crittografato, impostare questo su **null** o stringa vuota.

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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
