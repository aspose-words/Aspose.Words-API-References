---
title: "Aspose::Words::Saving::MarkdownExportAsHtml enum"
linktitle: "MarkdownExportAsHtml"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownExportAsHtml enum. C++'da Markdown'a ham HTML olarak dışa aktarılacak öğeleri belirtmeye izin verir."
type: docs
weight: 66500
url: /tr/cpp/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enum


Markdown'a ham HTML olarak dışa aktarılacak öğeleri belirtmeye izin verir.

```cpp
enum class MarkdownExportAsHtml
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Herhangi bir ham HTML olmadan Markdown sözdizimini kullanarak tüm öğeleri dışa aktar. |
| Tablolar | 1 | Tabloları ham HTML olarak dışa aktar. |
| NonCompatibleTables | 2 | Saf Markdown'te doğru şekilde temsil edilemeyen tabloları ham HTML olarak dışa aktar. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
