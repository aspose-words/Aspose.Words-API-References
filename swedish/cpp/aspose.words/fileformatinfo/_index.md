---
title: "Aspose::Words::FileFormatInfo klass"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatInfo klass. Innehåller data som returneras av FileFormatUtil:s metoder för dokumentformatdetektering. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 27000
url: /sv/cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


Innehåller data som returneras av [FileFormatUtil](../fileformatutil/) metoder för dokumentformatdetektering. För att lära dig mer, besök dokumentationsartikeln [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatInfo : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | Hämtar den upptäckta kodningen om den är tillämplig på det aktuella dokumentformatet. För närvarande upptäcker den kodning endast för HTML-dokument. |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | Returnerar **true** om detta dokument innehåller en digital signatur. Denna egenskap informerar bara om att en digital signatur finns på ett dokument, men den specificerar inte om signaturen är giltig eller inte. |
| [get_HasMacros](./get_hasmacros/)() const | Returnerar **true** om detta dokument innehåller VBA-makron. |
| [get_IsEncrypted](./get_isencrypted/)() const | Returnerar **true** om dokumentet är krypterat och kräver ett lösenord för att öppnas. |
| [get_LoadFormat](./get_loadformat/)() const | Hämtar det upptäckta dokumentformatet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Anmärkningar


Du skapar inte instanser av denna klass direkt. Objekt av denna klass returneras av [DetectFileFormat()](../) metoder.

## Exempel



Visar hur man använder [FileFormatUtil](../fileformatutil/) klassen för att upptäcka dokumentformatet och kryptering.
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


Visar hur man använder [FileFormatUtil](../fileformatutil/) klassen för att upptäcka dokumentformatet och förekomsten av digitala signaturer.
```cpp
// Använd en FileFormatInfo-instans för att verifiera att ett dokument inte är digitalt signerat.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Använd en ny FileFormatInstance för att bekräfta att den är signerad.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// Vi kan läsa in och komma åt signaturerna för ett signerat dokument i en samling på detta sätt.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
