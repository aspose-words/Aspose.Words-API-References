---
title: "Aspose::Words::Settings::WriteProtection klass"
linktitle: "WriteProtection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::WriteProtection klass. Anger inställningar för skrivskydd för ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


Anger inställningar för skrivskydd för ett dokument. För att lära dig mer, besök dokumentationsartikeln [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class WriteProtection : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | Returnerar **true** när ett skrivskyddslösenord har angetts. |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | Anger om dokumentförfattaren har rekommenderat att dokumentet ska öppnas som endast läsning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | Sättare för [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/). |
| [SetPassword](./setpassword/)(const System::String\&) | Ställer in skrivskyddslösenordet för dokumentet. |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | Returnerar **true** om det angivna lösenordet är samma som skrivskyddslösenordet som dokumentet skyddades med. Om dokumentet inte är skrivskyddat med lösenord returneras **false**. |
## Anmärkningar


Skrivskydd anger om författaren har rekommenderat att dokumentet ska öppnas som endast läsning och/eller kräva ett lösenord för att ändra dokumentet.

Skrivskydd är annorlunda än dokumentskydd. Skrivskydd anges i Microsoft Word i alternativ för dialogrutan Spara som.

Du skapar inte instanser av den här klassen direkt. Du får åtkomst till dokumentskyddsinställningarna via egenskapen [WriteProtection](../../aspose.words/document/get_writeprotection/).

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
