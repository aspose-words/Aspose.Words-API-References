---
title: "Aspose::Words::Settings::WriteProtection::get_IsWriteProtected Methode"
linktitle: "get_IsWriteProtected"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::WriteProtection::get_IsWriteProtected Methode. Gibt true zurück, wenn ein Schreibschutz‑Passwort in C++ gesetzt ist."
type: docs
weight: 2000
url: /de/cpp/aspose.words.settings/writeprotection/get_iswriteprotected/
---
## WriteProtection::get_IsWriteProtected method


Gibt **true** zurück, wenn ein Schreibschutz-Passwort festgelegt ist.

```cpp
bool Aspose::Words::Settings::WriteProtection::get_IsWriteProtected()
```


## Beispiele



Zeigt, wie ein Dokument mit einem Passwort geschützt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Geben Sie ein Passwort mit einer Länge von bis zu 15 Zeichen ein und überprüfen Sie anschließend den Schutzstatus des Dokuments.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// Der Schutz verhindert nicht, dass das Dokument programmgesteuert bearbeitet wird, und verschlüsselt den Inhalt nicht.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## Siehe auch

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
