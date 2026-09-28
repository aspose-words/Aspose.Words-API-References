---
title: "Метод Aspose::Words::Document::get_PageCount"
linktitle: "get_PageCount"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_PageCount. Получает количество страниц в документе, рассчитанное последней операцией компоновки страниц в C++."
type: docs
weight: 43000
url: /ru/cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


Получает количество страниц в документе, рассчитанное последней операцией компоновки страниц.

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## Примеры



Показывает, как подсчитать количество страниц в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Проверьте ожидаемое количество страниц документа.
ASSERT_EQ(3, doc->get_PageCount());

// Получение свойства PageCount вызывает компоновку страниц документа для вычисления значения.
// Эту операцию не потребуется выполнять повторно при рендеринге документа в фиксированный формат сохранения страниц,
// например, .pdf. Таким образом, вы можете сэкономить время, особенно при работе со сложными документами.
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
