---
title: "Aspose::Words::Saving::ImlRenderingMode enum"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImlRenderingMode enum. Anger hur bläck (InkML)-objekt renderas till fasta sidformat i C++."
type: docs
weight: 66000
url: /sv/cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


Anger hur bläck (InkML)-objekt renderas till fasta sidformat.

```cpp
enum class ImlRenderingMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Fallback | 0 | Om en reservform är tillgänglig för bläck (InkML)-objektet, renderar Aspose.Words reservformen istället för InkML. |
| InkML | 1 | Aspose.Words ignorerar reservformen för bläck (InkML)-objektet och renderar InkML själv. Detta är standardläget. |


## Exempel



Visar hur man renderar Ink-objekt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// Ställ in 'ImlRenderingMode.InkML' ignorerar reservformen för bläck (InkML)-objektet och renderar InkML själv.
// Om renderingsresultatet är otillfredsställande,
// vänligen använd 'ImlRenderingMode.Fallback' för att få ett resultat liknande tidigare versioner.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
