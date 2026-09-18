---
title: "Aspose::Words::FileFormatInfo::get_LoadFormat-Methode"
linktitle: "get_LoadFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatInfo::get_LoadFormat-Methode. Gibt das erkannte Dokumentformat in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words/fileformatinfo/get_loadformat/
---
## FileFormatInfo::get_LoadFormat method


Liest das erkannte Dokumentformat.

```cpp
Aspose::Words::LoadFormat Aspose::Words::FileFormatInfo::get_LoadFormat() const
```

## Hinweise


Wenn ein OOXML-Dokument verschlüsselt ist, kann man nicht feststellen, ob es sich um ein Excel-, Word- oder PowerPoint-Dokument handelt, ohne es zuerst zu entschlüsseln. Daher gibt diese Eigenschaft bei einem verschlüsselten OOXML-Dokument stets [Docx](../../loadformat/) zurück.

## Beispiele



Zeigt, wie man die Klasse [FileFormatUtil](../../fileformatutil/) verwendet, um das Dokumentformat und die Verschlüsselung zu erkennen.
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


Zeigt, wie die Methoden von [FileFormatUtil](../../fileformatutil/) verwendet werden, um das Format eines Dokuments zu erkennen.
```cpp
// Laden Sie ein Dokument aus einer Datei, der die Dateierweiterung fehlt, und erkennen Sie anschließend ihr Dateiformat.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Nachfolgend sind zwei Methoden zum Konvertieren eines LoadFormat in das entsprechende SaveFormat aufgeführt.
    // 1 -  Erhalte die Dateierweiterungszeichenkette für das LoadFormat und erhalte dann das entsprechende SaveFormat aus dieser Zeichenkette:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Konvertiere das LoadFormat direkt zu seinem SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Lade ein Dokument aus dem Stream und speichere es anschließend mit der automatisch erkannten Dateierweiterung.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## Siehe auch

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
