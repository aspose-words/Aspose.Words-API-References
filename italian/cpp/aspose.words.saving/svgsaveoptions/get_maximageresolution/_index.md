---
title: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution metodo"
linktitle: "get_MaxImageResolution"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution metodo. Ottiene o imposta un valore in pixel per pollice che limita la risoluzione delle immagini raster esportate. Il valore predefinito è zero in C++."
type: docs
weight: 4500
url: /it/cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


Ottiene o imposta un valore in pixel per pollice che limita la risoluzione delle immagini raster esportate. Il valore predefinito è zero.

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## Note


Se il valore di questa proprietà è diverso da zero, limita la risoluzione delle immagini raster esportate. Cioè, le immagini ad alta risoluzione vengono ricampionate verso il limite e le immagini a bassa risoluzione vengono esportate così come sono.

Se il valore di questa proprietà è zero, tutte le immagini raster vengono esportate senza ricampionamento.

## Esempi



Mostra come impostare il limite per la risoluzione delle immagini.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Vedi anche

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
