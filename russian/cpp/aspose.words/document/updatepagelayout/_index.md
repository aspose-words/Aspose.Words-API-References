---
title: "Aspose::Words::Document::UpdatePageLayout метод"
linktitle: "UpdatePageLayout"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::UpdatePageLayout метод. Перестраивает макет страниц документа в C++."
type: docs
weight: 98000
url: /ru/cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


Перестраивает разметку страниц документа.

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## Примечания


Этот метод форматирует документ по страницам и обновляет поля, связанные с номерами страниц в документе, такие как PAGE, PAGES, PAGEREF и REF. Актуальная информация о макете страниц необходима для корректного отображения документа в форматах фиксированных страниц.

Этот метод вызывается автоматически при первом преобразовании документа в PDF, XPS, изображение или при печати. Однако если вы измените документ после рендеринга и затем попытаетесь отрендерить его снова, Aspose.Words не обновит макет страниц автоматически. В этом случае следует вызвать [UpdatePageLayout](./) перед повторным рендерингом.

## Примеры



Показывает, когда необходимо пересчитать макет страниц документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Сохранение документа в PDF, в изображение или печать в первый раз будет автоматически
// кешировать макет документа в его страницах.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Измените документ каким-либо образом.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// В текущей версии Aspose.Words изменение документа не приводит к автоматическому пересозданию
// кешированный макет страницы. Если мы хотим, чтобы кешированный макет
// чтобы оставаться актуальным, нам придётся обновлять его вручную.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
