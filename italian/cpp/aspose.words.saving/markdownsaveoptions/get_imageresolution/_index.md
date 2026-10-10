---
title: "Metodo Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution"
linktitle: "get_ImageResolution"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution. Specifica la risoluzione di output per le immagini durante l'esportazione in Markdown. Il valore predefinito è %96 dpi in C++."
type: docs
weight: 3750
url: /it/cpp/aspose.words.saving/markdownsaveoptions/get_imageresolution/
---
## MarkdownSaveOptions::get_ImageResolution method


Specifica la risoluzione di output per le immagini durante l'esportazione in Markdown. Il valore predefinito è **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution() const
```


## Esempi



Mostra come impostare la risoluzione di output per le immagini.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

## Vedi anche

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
