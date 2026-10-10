---
title: "Aspose::Words::Loading::LoadOptions::get_Password Methode"
linktitle: "get_Password"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_Password Methode. Liest oder setzt das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann null oder ein leerer String sein. Standard ist null in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


Liest oder setzt das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann **null** oder ein leerer String sein. Standard ist **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## Hinweise


Sie müssen das Passwort kennen, um ein verschlüsseltes Dokument zu öffnen. Wenn das Dokument nicht verschlüsselt ist, setzen Sie dies auf **null** oder einen leeren String.

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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
