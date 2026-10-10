---
title: "Metodo Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder"
linktitle: "get_ResourcesFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder. Specifica la cartella fisica in cui le risorse (immagini) vengono salvate durante l'esportazione di un documento in formato Svg. Il valore predefinito è null in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/svgsaveoptions/get_resourcesfolder/
---
## SvgSaveOptions::get_ResourcesFolder method


Specifica la cartella fisica in cui le risorse (immagini) vengono salvate durante l'esportazione di un documento in formato SVG. Il valore predefinito è **null**.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder() const
```

## Note


Ha effetto solo se la proprietà [ExportEmbeddedImages](../get_exportembeddedimages/) è **false**.

Quando salvi un [Document](../../../aspose.words/document/) in formato SVG, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [ResourcesFolder](./) consente di specificare dove verranno salvate le immagini e [ResourcesFolderAlias](../get_resourcesfolderalias/) permette di specificare come verranno costruiti gli URI delle immagini.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Usa [ResourcesFolder](./) per sovrascrivere questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non dispone di una cartella in cui salvare le immagini, ma ha comunque bisogno di salvarle da qualche parte. In questo caso, è necessario specificare una cartella accessibile nella proprietà [ResourcesFolder](./).

## Vedi anche

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
