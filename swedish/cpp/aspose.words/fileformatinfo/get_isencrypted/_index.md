---
title: "Aspose::Words::FileFormatInfo::get_IsEncrypted metod"
linktitle: "get_IsEncrypted"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatInfo::get_IsEncrypted metod. Returnerar true om dokumentet är krypterat och kräver ett lösenord för att öppnas i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


Returnerar **true** om dokumentet är krypterat och kräver ett lösenord för att öppnas.

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## Anmärkningar


Denna egenskap finns för att hjälpa dig att sortera dokument som är krypterade från de som inte är det. Om du försöker läsa in ett krypterat dokument med Aspose.Words utan att ange ett lösenord kommer ett undantag att kastas. Du kan använda denna egenskap för att upptäcka om ett dokument kräver ett lösenord och vidta någon åtgärd innan du läser in dokumentet, till exempel be användaren om ett lösenord.

## Exempel



Visar hur man använder klassen [FileFormatUtil](../../fileformatutil/) för att upptäcka dokumentformatet och kryptering.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Konfigurera ett SaveOptions-objekt för att kryptera dokumentet
// med ett lösenord när vi sparar det, och sedan spara dokumentet.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Verifiera filtypen för vårt dokument och dess krypteringsstatus.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```

## Se även

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
