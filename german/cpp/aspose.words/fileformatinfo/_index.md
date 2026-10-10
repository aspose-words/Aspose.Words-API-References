---
title: "Aspose::Words::FileFormatInfo Klasse"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatInfo Klasse. Enthält Daten, die von den Dokumentformat-Erkennungsmethoden von FileFormatUtil zurückgegeben werden. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 27000
url: /de/cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


Enthält Daten, die von den Dokumentformat-Erkennungsmethoden von [FileFormatUtil](../fileformatutil/) zurückgegeben werden. Weitere Informationen finden Sie im Dokumentationsartikel [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatInfo : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | Liest die erkannte Kodierung, falls sie für das aktuelle Dokumentformat zutrifft. Derzeit wird die Kodierung nur für HTML-Dokumente erkannt. |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | Gibt **true** zurück, wenn dieses Dokument eine digitale Signatur enthält. Diese Eigenschaft informiert lediglich darüber, dass eine digitale Signatur im Dokument vorhanden ist, gibt jedoch nicht an, ob die Signatur gültig ist oder nicht. |
| [get_HasMacros](./get_hasmacros/)() const | Gibt **true** zurück, wenn dieses Dokument VBA‑Makros enthält. |
| [get_IsEncrypted](./get_isencrypted/)() const | Gibt **true** zurück, wenn das Dokument verschlüsselt ist und ein Passwort zum Öffnen benötigt. |
| [get_LoadFormat](./get_loadformat/)() const | Liest das erkannte Dokumentformat. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Hinweise


Sie erstellen keine Instanzen dieser Klasse direkt. Objekte dieser Klasse werden von den Methoden [DetectFileFormat()](../) zurückgegeben.

## Beispiele



Zeigt, wie die Klasse [FileFormatUtil](../fileformatutil/) verwendet wird, um das Dokumentformat und die Verschlüsselung zu erkennen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Konfigurieren Sie ein SaveOptions‑Objekt, um das Dokument zu verschlüsseln
// mit einem Passwort, wenn wir es speichern, und speichern Sie anschließend das Dokument.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Überprüfen Sie den Dateityp unseres Dokuments und dessen Verschlüsselungsstatus.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


Zeigt, wie die Klasse [FileFormatUtil](../fileformatutil/) verwendet wird, um das Dokumentformat und das Vorhandensein digitaler Signaturen zu erkennen.
```cpp
// Verwenden Sie eine FileFormatInfo-Instanz, um zu überprüfen, dass ein Dokument nicht digital signiert ist.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Verwenden Sie eine neue FileFormatInstance, um zu bestätigen, dass es signiert ist.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// Wir können die Signaturen eines signierten Dokuments in einer Sammlung wie folgt laden und darauf zugreifen.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
