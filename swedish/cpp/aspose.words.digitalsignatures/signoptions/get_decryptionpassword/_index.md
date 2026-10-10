---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword metod"
linktitle: "get_DecryptionPassword"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword metod. Lösenordet för att dekryptera källdokumentet. Standardvärdet är en tom sträng i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.digitalsignatures/signoptions/get_decryptionpassword/
---
## SignOptions::get_DecryptionPassword method


Lösenordet för att dekryptera källdokumentet. Standardvärdet är **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword() const
```


## Exempel



Visar hur man signerar en krypterad dokumentfil.
```cpp
// Skapa ett X.509‑certifikat från en PKCS#12‑butik, som bör innehålla en privat nyckel.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Skapa en kommentar, datum och dekrypteringslösenord som kommer att tillämpas med vår nya digitala signatur.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Ange ett lokalt systemfilnamn för det osignerade inmatningsdokumentet och ett utdatafilnamn för dess nya digitalt signerade kopia.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Se även

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
