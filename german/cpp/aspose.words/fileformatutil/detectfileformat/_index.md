---
title: "Aspose::Words::FileFormatUtil::DetectFileFormat method"
linktitle: "DetectFileFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatUtil::DetectFileFormat method. Ermittelt und gibt die Informationen über das Format eines in einem Stream gespeicherten Dokuments in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


Erkennt und gibt die Informationen über das Format eines in einem Stream gespeicherten Dokuments zurück.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Der Stream. |

### ReturnValue

Ein [FileFormatInfo](../../fileformatinfo/)-Objekt, das die erkannten Informationen enthält.
## Hinweise


Der Stream muss am Anfang des Dokuments positioniert sein.

Wenn diese Methode zurückkehrt, wird die Position im Stream auf die ursprüngliche Position zurückgesetzt.

Selbst wenn diese Methode das Dokumentformat erkennt, garantiert sie nicht, dass das angegebene Dokument gültig ist. Diese Methode erkennt das Dokumentformat nur, indem sie Daten liest, die für die Erkennung ausreichen. Um vollständig zu überprüfen, ob ein Dokument gültig ist, müssen Sie das Dokument in ein [Document](../../document/)-Objekt laden.

Diese Methode wirft [FileCorruptedException](../../filecorruptedexception/), wenn das Format erkannt wird, die Erkennung jedoch aufgrund von Beschädigungen nicht abgeschlossen werden kann.

## Beispiele



Zeigt, wie die [FileFormatUtil](../)-Methoden verwendet werden, um das Format eines Dokuments zu erkennen.
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

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


Erkennt und gibt die Informationen über das Format eines in einer Festplattendatei gespeicherten Dokuments zurück.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Der Dateiname. |

### ReturnValue

Ein [FileFormatInfo](../../fileformatinfo/)-Objekt, das die erkannten Informationen enthält.
## Hinweise


Selbst wenn diese Methode das Dokumentformat erkennt, garantiert sie nicht, dass das angegebene Dokument gültig ist. Diese Methode erkennt das Dokumentformat nur, indem sie Daten liest, die für die Erkennung ausreichen. Um vollständig zu überprüfen, ob ein Dokument gültig ist, müssen Sie das Dokument in ein [Document](../../document/)-Objekt laden.

Diese Methode wirft [FileCorruptedException](../../filecorruptedexception/), wenn das Format erkannt wird, die Erkennung jedoch aufgrund von Beschädigungen nicht abgeschlossen werden kann.

## Beispiele



Zeigt, wie die [FileFormatUtil](../)-Klasse verwendet wird, um das Dokumentformat und die Verschlüsselung zu erkennen.
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


Zeigt, wie die [FileFormatUtil](../)-Klasse verwendet wird, um das Dokumentformat und das Vorhandensein digitaler Signaturen zu erkennen.
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

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## Siehe auch

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
