---
title: "Aspose::Words::PageExtractOptions class"
linktitle: "PageExtractOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::PageExtractOptions. Позволяет задавать параметры извлечения страниц документа в C++."
type: docs
weight: 45500
url: /ru/cpp/aspose.words/pageextractoptions/
---
## PageExtractOptions class


Позволяет задавать параметры извлечения страниц документа.

```cpp
class PageExtractOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/)() const | Указывает, будут ли поля NUMPAGES в получаемом документе заменены их фактическими значениями. Значение по умолчанию — **true**. |
| [get_UpdatePageStartingNumber](./get_updatepagestartingnumber/)() const | Указывает, будет ли обновлен номер начальной страницы в получаемом документе. Значение по умолчанию — **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageExtractOptions](./pageextractoptions/)() |  |
| [set_UnlinkPagesNumberFields](./set_unlinkpagesnumberfields/)(bool) | Сеттер для [Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/). |
| [set_UpdatePageStartingNumber](./set_updatepagestartingnumber/)(bool) | Сеттер для [Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber](./get_updatepagestartingnumber/). |
| static [Type](./type/)() |  |

## Примеры



Показать, как сбросить начальную нумерацию страниц и сохранить поле NUMPAGE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// Поведение по умолчанию:
// Извлечённая нумерация страниц совпадает с оригинальным документом, как будто мы выбрали \"Print 2 pages\" в MS Word.
// Номер начальной страницы будет установлен в 2, а поле, указывающее количество страниц, будет удалено
// и заменено постоянным значением, равным количеству страниц.
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// Изменённое поведение:
// Извлечённая нумерация страниц сбрасывается, и начинается новая,
// как будто мы скопировали содержимое второй страницы и вставили его в новый документ.
// Номер начальной страницы будет установлен в 1, а поле, указывающее количество страниц, останется без изменений
// и будет показывать текущее количество страниц.
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
