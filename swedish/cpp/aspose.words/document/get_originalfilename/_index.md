---
title: "Aspose::Words::Document::get_OriginalFileName method"
linktitle: "get_OriginalFileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_OriginalFileName method. Hämtar det ursprungliga filnamnet för dokumentet i C++."
type: docs
weight: 40000
url: /sv/cpp/aspose.words/document/get_originalfilename/
---
## Document::get_OriginalFileName method


Hämtar det ursprungliga filnamnet för dokumentet.

```cpp
System::String Aspose::Words::Document::get_OriginalFileName() const
```

## Anmärkningar


Returnerar **null** om dokumentet lästes in från en ström eller skapades tomt.

## Exempel



Visar hur man hämtar detaljer om ett dokuments inläsningsoperation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```


Visar hur man använder [FileFormatUtil](../../fileformatutil/)‑metoderna för att upptäcka formatet på ett dokument.
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
