---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting method"
linktitle: "get_ExportUnderlineFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting method. Ottiene o imposta un valore booleano che indica se esportare la formattazione del testo sottolineato come sequenza di due caratteri più \"++\". Il valore predefinito è false in C++."
type: docs
weight: 3500
url: /it/cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


Ottiene o imposta un valore booleano che indica se esportare la formattazione del testo sottolineato come sequenza di due caratteri più "++". Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## Esempi



Mostra come esportare la formattazione del testo sottolineato come ++.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## Vedi anche

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
