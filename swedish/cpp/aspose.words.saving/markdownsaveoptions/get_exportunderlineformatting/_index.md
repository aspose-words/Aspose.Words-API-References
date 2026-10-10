---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting metod"
linktitle: "get_ExportUnderlineFormatting"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting metod. Hämtar eller anger ett booleskt värde som indikerar om understruken textformatering ska exporteras som en sekvens av två plustecken \"++\". Standardvärdet är false i C++."
type: docs
weight: 3500
url: /sv/cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


Hämtar eller anger ett booleskt värde som indikerar om understruken textformatering ska exporteras som en sekvens av två plustecken "++". Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## Exempel



Visar hur man exporterar understruken formatering som ++.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## Se även

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
