---
title: "Aspose::Words::Saving::OdtSaveOptions::get_Password Methode"
linktitle: "get_Password"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::OdtSaveOptions::get_Password Methode. Ruft ein Passwort ab oder legt es fest, um das Dokument in C++ zu verschlüsseln."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/odtsaveoptions/get_password/
---
## OdtSaveOptions::get_Password method


Liest oder legt ein Passwort zum Verschlüsseln des Dokuments fest.

```cpp
System::String Aspose::Words::Saving::OdtSaveOptions::get_Password() const
```

## Hinweise


Um ein Dokument ohne Verschlüsselung zu speichern, sollte diese Eigenschaft **null** oder ein leerer String sein.

## Beispiele



Zeigt, wie man ein gespeichertes ODT/OTT-Dokument mit einem Passwort verschlüsselt und es dann mit Aspose.Words lädt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Erstellen Sie ein neues OdtSaveOptions und übergeben Sie entweder \"SaveFormat.Odt\",
// oder \"SaveFormat.Ott\" als das Format, in dem das Dokument gespeichert werden soll.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// Wenn wir dieses Dokument mit einem geeigneten Editor öffnen,
// wird es uns nach dem Passwort fragen, das wir im SaveOptions-Objekt angegeben haben.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// Wenn wir dieses Dokument erneut mit Aspose.Words öffnen oder bearbeiten möchten,
// müssen wir dem Lade‑Konstruktor ein LoadOptions-Objekt mit dem korrekten Passwort übergeben.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Siehe auch

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
