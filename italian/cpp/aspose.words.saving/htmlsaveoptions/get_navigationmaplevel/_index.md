---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel metodo"
linktitle: "get_NavigationMapLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel metodo. Specifica il livello massimo di intestazioni inserite nella mappa di navigazione durante l'esportazione nei formati EPUB, MOBI o AZW3. Il valore predefinito è %3 in C++."
type: docs
weight: 40500
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


Specifica il livello massimo di intestazioni popolato nella mappa di navigazione durante l'esportazione nei formati EPUB, MOBI o AZW3. Il valore predefinito è **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## Note


La mappa di navigazione consente agli agenti utente di fornire un modo semplice per navigare nella struttura del documento. Di solito i punti di navigazione corrispondono alle intestazioni nel documento. Per inserire le intestazioni fino al livello **N** assegna questo valore a [NavigationMapLevel](./).

Per impostazione predefinita, vengono inseriti tre livelli di intestazioni: paragrafi con gli stili **Heading 1**, **Heading 2** e **Heading 3**. Puoi impostare questa proprietà a un valore da 1 a 9 per richiedere il livello massimo corrispondente. Impostandola a zero la mappa di navigazione verrà ridotta solo alla radice del documento o alle radici delle parti del documento.

## Esempi



Mostra come generare l'indice per i documenti Azw3.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Azw3);
options->set_NavigationMapLevel(2);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```


Mostra come generare l'indice per i documenti Mobi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mobi);
options->set_NavigationMapLevel(5);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateMobiToc.mobi", options);
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
