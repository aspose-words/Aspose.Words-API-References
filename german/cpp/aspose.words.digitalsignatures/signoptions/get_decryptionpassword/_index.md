---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword Methode"
linktitle: "get_DecryptionPassword"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword Methode. Das Passwort zum Entschlüsseln des Quelldokuments. Der Standardwert ist eine leere Zeichenkette in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.digitalsignatures/signoptions/get_decryptionpassword/
---
## SignOptions::get_DecryptionPassword method


Das Passwort zum Entschlüsseln des Quelldokuments. Standardwert ist **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword() const
```


## Beispiele



Zeigt, wie man eine verschlüsselte Dokumentdatei signiert.
```cpp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Store, der einen privaten Schlüssel enthalten sollte.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Erstellt einen Kommentar, ein Datum und ein Entschlüsselungspasswort, die mit unserer neuen digitalen Signatur angewendet werden.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Legt einen lokalen Systemdateinamen für das unsignierte Eingabedokument fest und einen Ausgabedateinamen für dessen neu digital signierte Kopie.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Siehe auch

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
