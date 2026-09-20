---
title: "Aspose::Words::DocumentBase::get_Document метод"
linktitle: "get_Document"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBase::get_Document метод. Возвращает этот экземпляр в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


Получает текущий экземпляр.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## Примеры



Показывает, как создать простой документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Новые объекты Document по умолчанию поставляются с минимальным набором узлов
// необходимы для начала добавления содержимого, такого как текст и фигуры: Section, Body и Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## См. также

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
