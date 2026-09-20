---
title: "Aspose::Words::Saving::MarkdownListExportMode перечисление"
linktitle: "MarkdownListExportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MarkdownListExportMode перечисление. Указывает, как списки экспортируются в Markdown в C++."
type: docs
weight: 68000
url: /ru/cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


Указывает, как списки экспортируются в Markdown.

```cpp
enum class MarkdownListExportMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| MarkdownSyntax | 0 | Экспортировать элементы списка, совместимые с синтаксисом Markdown. |
| PlainText | 1 | Экспортировать элементы списка как обычный текст. |


## Примеры



Показывает, как элементы списка будут записаны в markdown‑документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Используйте MarkdownListExportMode.PlainText или MarkdownListExportMode.MarkdownSyntax для экспорта списка.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
