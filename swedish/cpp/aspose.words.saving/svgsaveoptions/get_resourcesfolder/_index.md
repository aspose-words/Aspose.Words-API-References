---
title: "Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder metod"
linktitle: "get_ResourcesFolder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder metod. Anger den fysiska mappen där resurser (bilder) sparas när ett dokument exporteras till Svg-format. Standard är null i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/svgsaveoptions/get_resourcesfolder/
---
## SvgSaveOptions::get_ResourcesFolder method


Anger den fysiska mappen där resurser (bilder) sparas när ett dokument exporteras till Svg-format. Standard är **null**.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder() const
```

## Anmärkningar


Har effekt endast om egenskapen [ExportEmbeddedImages](../get_exportembeddedimages/) är **false**.

När du sparar ett [Document](../../../aspose.words/document/) i SVG-format måste Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer. [ResourcesFolder](./) låter dig ange var bilderna ska sparas och [ResourcesFolderAlias](../get_resourcesfolderalias/) låter dig ange hur bild-URI:erna ska konstrueras.

Om du sparar ett dokument till en fil och anger ett filnamn sparar Aspose.Words som standard bilderna i samma mapp där dokumentfilen sparas. Använd [ResourcesFolder](./) för att åsidosätta detta beteende.

Om du sparar ett dokument till en ström har Aspose.Words ingen mapp att spara bilderna i, men måste ändå spara bilderna någonstans. I så fall måste du ange en åtkomlig mapp i egenskapen [ResourcesFolder](./).

## Se även

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
