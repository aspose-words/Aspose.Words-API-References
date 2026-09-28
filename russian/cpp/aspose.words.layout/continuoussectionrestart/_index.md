---
title: "Aspose::Words::Layout::ContinuousSectionRestart enum"
linktitle: "ContinuousSectionRestart"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::ContinuousSectionRestart enum. Представляет различные варианты поведения при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


Представляет различные поведения при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц.

```cpp
enum class ContinuousSectionRestart
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Всегда | 0 | Нумерация страниц всегда перезапускается независимо от потока содержимого. |
| FromNewPageOnly | 1 | Нумерация страниц перезапускается только если перед разделом на странице, где начинается раздел, нет другого содержимого. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
