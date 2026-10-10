---
title: "Aspose::Words::FileFormatInfo::get_IsEncrypted-Methode"
linktitle: "get_IsEncrypted"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatInfo::get_IsEncrypted-Methode. Gibt true zurück, wenn das Dokument verschlüsselt ist und ein Passwort zum Öffnen in C++ benötigt."
type: docs
weight: 4000
url: /de/cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


Gibt **true** zurück, wenn das Dokument verschlüsselt ist und ein Passwort zum Öffnen benötigt.

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## Hinweise


Diese Eigenschaft dient dazu, verschlüsselte Dokumente von nicht verschlüsselten zu unterscheiden. Wenn Sie versuchen, ein verschlüsseltes Dokument mit Aspose.Words zu laden, ohne ein Passwort anzugeben, wird eine Ausnahme ausgelöst. Sie können diese Eigenschaft verwenden, um zu erkennen, ob ein Dokument ein Passwort benötigt, und vor dem Laden des Dokuments entsprechende Maßnahmen ergreifen, zum Beispiel den Benutzer nach einem Passwort fragen.

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

## Siehe auch

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
