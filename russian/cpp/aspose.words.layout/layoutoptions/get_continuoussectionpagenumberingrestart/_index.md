---
title: "метод Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart"
linktitle: "get_ContinuousSectionPageNumberingRestart"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart. Получает или задает режим поведения при вычислении номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


Получает или задает режим поведения при вычислении номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц.

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


## Примеры



Показывает, как управлять нумерацией страниц в непрерывном разделе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// По умолчанию поведение Aspose.Words соответствует Microsoft Word 2019.
// Если вам нужно старое поведение Aspose.Words, аналогичное Microsoft Word 2016, используйте 'ContinuousSectionRestart.FromNewPageOnly'.
// Нумерация страниц перезапускается только если перед разделом на странице, где начинается раздел, нет другого содержимого,
// из‑за этого нумерация будет сбрасываться до 2 со второй страницы.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## См. также

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
