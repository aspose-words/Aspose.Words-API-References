---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution Methode"
linktitle: "get_ImageResolution"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution Methode. Gibt die Ausgaberesolution für Bilder beim Export nach Markdown an. Der Standardwert ist %96 dpi in C++."
type: docs
weight: 3750
url: /de/cpp/aspose.words.saving/markdownsaveoptions/get_imageresolution/
---
## MarkdownSaveOptions::get_ImageResolution method


Gibt die Ausgaberesolution für Bilder beim Export nach Markdown an. Standard ist **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution() const
```


## Beispiele



Zeigt, wie man die Ausgaberesolution für Bilder festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

## Siehe auch

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
