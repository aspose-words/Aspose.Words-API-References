---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode yöntemi"
linktitle: "get_LinkExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode yöntemi. Bağlantıların çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer C++'ta Auto'dur."
type: docs
weight: 5750
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/get_linkexportmode/
---
## MarkdownSaveOptions::get_LinkExportMode method


Bağlantıların çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer [Auto](../../markdownlinkexportmode/).

```cpp
Aspose::Words::Saving::MarkdownLinkExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode() const
```


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

* Enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
