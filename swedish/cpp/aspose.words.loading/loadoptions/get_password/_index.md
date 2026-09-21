---
title: "Aspose::Words::Loading::LoadOptions::get_Password metod"
linktitle: "get_Password"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_Password metod. Hämtar eller anger lösenordet för att öppna ett krypterat dokument. Kan vara null eller en tom sträng. Standard är null i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


Hämtar eller anger lösenordet för att öppna ett krypterat dokument. Kan vara **null** eller en tom sträng. Standardvärdet är **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## Anmärkningar


Du måste känna till lösenordet för att öppna ett krypterat dokument. Om dokumentet inte är krypterat, sätt detta till **null** eller en tom sträng.

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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
