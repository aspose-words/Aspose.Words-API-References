---
title: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator конструктор"
linktitle: "LayoutEnumerator"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator конструктор. Инициализирует новый экземпляр этого класса в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator::LayoutEnumerator constructor


Инициализирует новый экземпляр этого класса.

```cpp
Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator(const System::SharedPtr<Aspose::Words::Document> &document)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| документ | const System::SharedPtr\<Aspose::Words::Document\>\& | Документ, модель разметки страниц которого нужно перечислять. |
## Примечания


Если модель разметки страниц документа не построена, перечислитель вызывает [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/), чтобы построить её.

Каждый раз, когда документ обновляется и создаётся новая модель разметки страниц, необходимо использовать новый перечислитель для доступа к ней.

## См. также

* Class [Document](../../../aspose.words/document/)
* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
