---
title: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature metod"
linktitle: "get_HasDigitalSignature"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatInfo::get_HasDigitalSignature metod. Returnerar true om detta dokument innehåller en digital signatur. Denna egenskap informerar endast om att en digital signatur finns på ett dokument, men den specificerar inte om signaturen är giltig eller inte i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo::get_HasDigitalSignature method


Returnerar **true** om detta dokument innehåller en digital signatur. Denna egenskap informerar bara om att en digital signatur finns på ett dokument, men den specificerar inte om signaturen är giltig eller inte.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```

## Anmärkningar


Denna egenskap finns för att hjälpa dig att sortera dokument som är digitalt signerade från de som inte är det. Om du använder Aspose.Words för att ändra och spara ett dokument som är digitalt signerat, kommer den digitala signaturen att gå förlorad. Detta är avsiktligt eftersom en digital signatur finns för att skydda ett dokuments äkthet. Genom att använda denna egenskap kan du upptäcka digitalt signerade dokument innan du behandlar dem på samma sätt som vanliga dokument och vidta åtgärder för att undvika att den digitala signaturen förloras, till exempel meddela användaren.

## Exempel



Visar hur man använder klassen [FileFormatUtil](../../fileformatutil/) för att upptäcka dokumentformatet och närvaron av digitala signaturer.
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

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
