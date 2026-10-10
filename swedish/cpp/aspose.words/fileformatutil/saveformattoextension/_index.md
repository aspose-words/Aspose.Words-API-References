---
title: "Aspose::Words::FileFormatUtil::SaveFormatToExtension metod"
linktitle: "SaveFormatToExtension"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatUtil::SaveFormatToExtension metod. Konverterar ett sparaformat-uppräkningsvärde till en filändelse. Den returnerade ändelsen är en gemenersträng med en inledande punkt i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil::SaveFormatToExtension method


Konverterar ett enumererat värde för sparaformat till en filändelse. Den returnerade ändelsen är en gemener sträng med en inledande punkt.

```cpp
static System::String Aspose::Words::FileFormatUtil::SaveFormatToExtension(Aspose::Words::SaveFormat saveFormat)
```

## Anmärkningar


Värdet [WordML](../../saveformat/) konverteras till \".wml\".

Värdet [FlatOpc](../../saveformat/) konverteras till \".fopc\".

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

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
