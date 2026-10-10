---
title: "Aspose::Words::Saving::MarkdownListExportMode enum"
linktitle: "MarkdownListExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownListExportMode enum. Listelerin C++'da Markdown formatına nasıl dışa aktarıldığını belirtir."
type: docs
weight: 68000
url: /tr/cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


Listelerin Markdown'a nasıl dışa aktarıldığını belirtir.

```cpp
enum class MarkdownListExportMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| MarkdownSyntax | 0 | Markdown sözdizimiyle uyumlu liste öğelerini dışa aktar. |
| DüzMetin | 1 | Liste öğelerini düz metin olarak dışa aktar. |


## Örnekler



Liste öğelerinin markdown belgesine nasıl yazılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Listeyi dışa aktarmak için MarkdownListExportMode.PlainText veya MarkdownListExportMode.MarkdownSyntax kullanın.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
