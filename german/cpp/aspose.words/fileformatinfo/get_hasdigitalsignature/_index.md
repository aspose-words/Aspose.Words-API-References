---
title: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature-Methode"
linktitle: "get_HasDigitalSignature"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature-Methode. Gibt true zurück, wenn dieses Dokument eine digitale Signatur enthält. Diese Eigenschaft informiert lediglich darüber, dass eine digitale Signatur im Dokument vorhanden ist, gibt jedoch nicht an, ob die Signatur gültig ist oder nicht in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo::get_HasDigitalSignature method


Gibt **true** zurück, wenn dieses Dokument eine digitale Signatur enthält. Diese Eigenschaft informiert lediglich darüber, dass eine digitale Signatur im Dokument vorhanden ist, gibt jedoch nicht an, ob die Signatur gültig ist oder nicht.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```

## Hinweise


Diese Eigenschaft dient dazu, digital signierte Dokumente von nicht signierten zu unterscheiden. Wenn Sie Aspose.Words verwenden, um ein digital signiertes Dokument zu ändern und zu speichern, geht die digitale Signatur verloren. Das ist beabsichtigt, da eine digitale Signatur zum Schutz der Authentizität eines Dokuments dient. Mit dieser Eigenschaft können Sie digital signierte Dokumente erkennen, bevor Sie sie wie normale Dokumente verarbeiten, und Maßnahmen ergreifen, um den Verlust der digitalen Signatur zu vermeiden, zum Beispiel den Benutzer benachrichtigen.

## Beispiele



Zeigt, wie man die Klasse [FileFormatUtil](../../fileformatutil/) verwendet, um das Dokumentformat und das Vorhandensein digitaler Signaturen zu erkennen.
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

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
