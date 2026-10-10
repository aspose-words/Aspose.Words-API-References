---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml yöntemi"
linktitle: "get_ExportAsHtml"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml yöntemi. Öğelerin Markdown'a ham HTML olarak dışa aktarılmasını belirtmenizi sağlar. Varsayılan değer C++'ta None'dur."
type: docs
weight: 2500
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/get_exportashtml/
---
## MarkdownSaveOptions::get_ExportAsHtml method


Öğelerin Markdown'a ham HTML olarak dışa aktarılmasını belirtmenizi sağlar. Varsayılan değer [None](../../markdownexportashtml/).

```cpp
Aspose::Words::Saving::MarkdownExportAsHtml Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml() const
```


## Örnekler



Bir tabloyu Markdown'a ham HTML olarak nasıl dışa aktarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// Tablo oluştur.
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportAsHtml(Aspose::Words::Saving::MarkdownExportAsHtml::Tables);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

## Ayrıca Bakınız

* Enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
