---
title: "Метод Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode"
linktitle: "get_ListExportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode. Указывает, как элементы списка будут записываться в выходной файл. Значение по умолчанию — MarkdownSyntax в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


Указывает, как элементы списка будут записываться в выходной файл. Значение по умолчанию — [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## Примечания


Когда это свойство установлено в значение [PlainText](../../markdownlistexportmode/), все метки списка обновляются с помощью [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) и экспортируются с их фактическими значениями. Такие списки могут быть несовместимы с форматом Markdown и будут распознаны как обычный текст при импорте в этом случае.

Когда это свойство установлено в значение [MarkdownSyntax](../../markdownlistexportmode/), записывающий модуль пытается экспортировать элементы списка таким образом, чтобы их можно было нумеровать в автоматическом режиме с помощью Markdown.

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

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
