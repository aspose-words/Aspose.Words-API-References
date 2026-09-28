---
title: "Метод Aspose::Words::Document::ExtractPages"
linktitle: "ExtractPages"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::ExtractPages. Возвращает объект Document, представляющий указанный диапазон страниц, в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


Возвращает объект [Document](../), представляющий указанный диапазон страниц.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Нулевой индекс первой страницы для извлечения. |
| count | int32_t | Количество страниц для извлечения. |

## Примеры



Показывает, как получить указанный диапазон страниц из документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


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

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


Возвращает объект [Document](../), представляющий указанный диапазон страниц и заданные параметры извлечения страниц.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Нулевой индекс первой страницы для извлечения. |
| count | int32_t | Количество страниц для извлечения. |
| параметры | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | Предоставляет параметры для управления процессом извлечения страниц. |

## См. также

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
