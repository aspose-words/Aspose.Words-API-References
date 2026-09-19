---
title: "Aspose::Words::Saving::MarkdownLinkExportMode enum"
linktitle: "MarkdownLinkExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MarkdownLinkExportMode enum. Specifica come i collegamenti vengono esportati in Markdown in C++."
type: docs
weight: 67000
url: /it/cpp/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enum


Specifica come i collegamenti vengono esportati in Markdown.

```cpp
enum class MarkdownLinkExportMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | 0 | Rileva automaticamente la modalità di esportazione per ogni collegamento. |
| Inline | 1 | Esporta tutti i collegamenti come blocchi in linea. |
| Riferimento | 2 | Esporta tutti i collegamenti come blocchi di riferimento. |


## Esempi



Mostra come i collegamenti verranno scritti nel file .md.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 100, 100);

// L'immagine verrà scritta come riferimento:
// ![ref1]
// [ref1]: aw_ref.001.png
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Reference);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// L'immagine verrà scritta in linea:
// ![](aw_inline.001.png)
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Inline);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
