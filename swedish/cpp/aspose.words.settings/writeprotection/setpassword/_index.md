---
title: "Aspose::Words::Settings::WriteProtection::SetPassword metod"
linktitle: "SetPassword"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::WriteProtection::SetPassword metod. Anger lösenordet för skrivskydd för dokumentet i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection::SetPassword method


Ställer in skrivskyddslösenordet för dokumentet.

```cpp
void Aspose::Words::Settings::WriteProtection::SetPassword(const System::String &password)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| password | const System::String\& | Lösenordet att ange. Kan inte vara **null**, men kan vara en tom sträng. |
## Anmärkningar


Om ett lösenord har angetts kommer Microsoft Word att kräva att användaren anger det eller öppnar dokumentet som skrivskyddat.

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
