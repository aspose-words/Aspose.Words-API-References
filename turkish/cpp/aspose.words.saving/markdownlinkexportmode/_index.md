---
title: "Aspose::Words::Saving::MarkdownLinkExportMode enum"
linktitle: "MarkdownLinkExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownLinkExportMode enum. Bağlantıların C++'da Markdown'a nasıl dışa aktarıldığını belirtir."
type: docs
weight: 67000
url: /tr/cpp/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enum


Bağlantıların Markdown'a nasıl dışa aktarıldığını belirtir.

```cpp
enum class MarkdownLinkExportMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Otomatik | 0 | Her bağlantı için dışa aktarma modunu otomatik olarak algıla. |
| Satır içi | 1 | Tüm bağlantıları satır içi bloklar olarak dışa aktar. |
| Referans | 2 | Tüm bağlantıları referans blokları olarak dışa aktar. |


## Örnekler



Bağlantıların .md dosyasına nasıl yazılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 100, 100);

// Görsel referans olarak yazılacak:
// ![ref1]
// [ref1]: aw_ref.001.png
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Reference);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// Görsel satır içi olarak yazılacak:
// ![](aw_inline.001.png)
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Inline);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
