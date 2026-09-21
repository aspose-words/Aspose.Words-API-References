---
title: "Aspose::Words::LoadFormat enum"
linktitle: "LoadFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LoadFormat enum. Anger formatet på dokumentet som ska laddas i C++."
type: docs
weight: 97000
url: /sv/cpp/aspose.words/loadformat/
---
## LoadFormat enum


Anger formatet för dokumentet som ska laddas.

```cpp
enum class LoadFormat
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | 0 | Instruerar Aspose.Words att känna igen formatet automatiskt. |
| MsWorks | 8 | Microsoft Works 8 [Dokument](../document/). |
| Doc | 10 | Microsoft Word 95 eller Word 97 - 2003 [Dokument](../document/). |
| Dot | 11 | Microsoft Word 95 eller Word 97 - 2003 mall. |
| DocPreWord60 | 12 | Dokumentet är i pre-Word 95-format. Aspose.Words stöder för närvarande inte inläsning av sådana dokument. |
| Docx | 20 | Office Open XML WordprocessingML [Dokument](../document/) (utan makron). |
| Docm | 21 | Office Open XML WordprocessingML med makron [Dokument](../document/). |
| Dotx | 22 | Office Open XML WordprocessingML-mall (utan makron). |
| Dotm | 23 | Office Open XML WordprocessingML-mall med makron. |
| FlatOpc | 24 | Office Open XML WordprocessingML lagrad i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML med makron [Dokument](../document/) lagrad i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplate | 26 | Office Open XML WordprocessingML-mall (utan makron) lagrad i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplateMacroEnabled | 27 | Office Open XML WordprocessingML-mall med makron lagrad i en platt XML-fil istället för ett ZIP-paket. |
| Rtf | 30 | RTF-format. |
| WordML | 31 | Microsoft Word 2003 WordprocessingML-format. |
| Html | 50 | HTML-format. |
| Mhtml | 51 | MHTML (webarkiv) format. |
| Mobi | 52 | MOBI-format. Används av MobiPocket-läsaren och Amazon Kindle-läsare. |
| Chm | 53 | CHM (kompilerad HTML-hjälp) format. |
| Azw3 | 54 | AZW3-format. Används av Amazon Kindle-läsare. |
| Epub | 55 | EPUB-format. |
| Odt | 60 | ODF Text [Document](../document/). |
| Ott | 61 | ODF Text [Document](../document/) mall. |
| Text | 62 | Oren text. |
| Markdown | 63 | Markdown-textdokument. |
| Xml | 65 | XML-dokument. |
| Unknown | 255 | Okänt format, kan inte laddas av [Aspose.Words](../). |


## Exempel



Visar hur man använder [FileFormatUtil](../fileformatutil/)-metoderna för att upptäcka formatet på ett dokument.
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


Visar hur man anger en bas‑URI när man öppnar ett html‑dokument.
```cpp
// Anta att vi vill läsa in ett .html‑dokument som innehåller en bild länkad med en relativ URI
// medan bilden finns på en annan plats. I så fall måste vi omvandla den relativa URI:n till en absolut.
// Vi kan ange en bas‑URI med ett HtmlLoadOptions‑objekt.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Även om bilden var trasig i den inmatade .html‑filen, hjälpte vår anpassade bas‑URI oss att reparera länken.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Detta utdata‑dokument kommer att visa bilden som saknades.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
