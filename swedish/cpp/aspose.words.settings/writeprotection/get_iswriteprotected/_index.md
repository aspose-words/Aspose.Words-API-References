---
title: "Aspose::Words::Settings::WriteProtection::get_IsWriteProtected metod"
linktitle: "get_IsWriteProtected"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::WriteProtection::get_IsWriteProtected metod. Returnerar true när ett skrivskyddslösenord har angetts i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.settings/writeprotection/get_iswriteprotected/
---
## WriteProtection::get_IsWriteProtected method


Returnerar **true** när ett skrivskyddslösenord har angetts.

```cpp
bool Aspose::Words::Settings::WriteProtection::get_IsWriteProtected()
```


## Exempel



Visar hur man skyddar ett dokument med ett lösenord.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Ange ett lösenord på högst 15 tecken och verifiera sedan dokumentets skyddstatus.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// Skydd hindrar inte dokumentet från att redigeras programmässigt, och det krypterar inte heller innehållet.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## Se även

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
