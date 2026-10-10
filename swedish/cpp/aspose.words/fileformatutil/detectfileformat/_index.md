---
title: "Aspose::Words::FileFormatUtil::DetectFileFormat metod"
linktitle: "DetectFileFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatUtil::DetectFileFormat metod. Detekterar och returnerar information om ett format för ett dokument som lagras i en ström i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


Detekterar och returnerar information om formatet för ett dokument som lagras i en ström.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | Strömmen. |

### ReturnValue

Ett [FileFormatInfo](../../fileformatinfo/)‑objekt som innehåller den upptäckta informationen.
## Anmärkningar


Strömmen måste vara placerad i början av dokumentet.

När denna metod returnerar återställs positionen i strömmen till den ursprungliga positionen.

Även om denna metod upptäcker dokumentformatet garanterar den inte att det angivna dokumentet är giltigt. Metoden upptäcker endast dokumentformatet genom att läsa data som är tillräcklig för upptäckt. För att fullt ut verifiera att ett dokument är giltigt måste du läsa in dokumentet i ett [Document](../../document/)‑objekt.

Denna metod kastar [FileCorruptedException](../../filecorruptedexception/) när formatet känns igen, men upptäckten kan inte slutföras på grund av korruption.

## Exempel



Visar hur man använder [FileFormatUtil](../)-metoderna för att upptäcka formatet på ett dokument.
```cpp
// Läs in ett dokument från en fil som saknar filändelse och upptäck sedan dess filformat.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Nedan följer två metoder för att konvertera ett LoadFormat till motsvarande SaveFormat.
    // 1 -  Hämta filändelse‑strängen för LoadFormat, och hämta sedan motsvarande SaveFormat från den strängen:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Konvertera LoadFormat direkt till dess SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Läs in ett dokument från strömmen och spara det sedan till den automatiskt upptäckta filändelsen.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## Se även

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


Detekterar och returnerar information om formatet för ett dokument som lagras i en diskfil.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | const System::String\& | Filnamnet. |

### ReturnValue

Ett [FileFormatInfo](../../fileformatinfo/)‑objekt som innehåller den upptäckta informationen.
## Anmärkningar


Även om denna metod upptäcker dokumentformatet garanterar den inte att det angivna dokumentet är giltigt. Metoden upptäcker endast dokumentformatet genom att läsa data som är tillräcklig för upptäckt. För att fullt ut verifiera att ett dokument är giltigt måste du läsa in dokumentet i ett [Document](../../document/)‑objekt.

Denna metod kastar [FileCorruptedException](../../filecorruptedexception/) när formatet känns igen, men upptäckten kan inte slutföras på grund av korruption.

## Exempel



Visar hur man använder klassen [FileFormatUtil](../) för att upptäcka dokumentformatet och kryptering.
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


Visar hur man använder klassen [FileFormatUtil](../) för att upptäcka dokumentformatet och närvaron av digitala signaturer.
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

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## Se även

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
