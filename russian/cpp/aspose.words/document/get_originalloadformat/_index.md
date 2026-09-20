---
title: "Aspose::Words::Document::get_OriginalLoadFormat метод"
linktitle: "get_OriginalLoadFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_OriginalLoadFormat. Получает формат исходного документа, загруженного в этот объект в C++."
type: docs
weight: 41000
url: /ru/cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


Получает формат исходного документа, загруженного в этот объект.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## Примечания


Если вы создали новый пустой документ, возвращает значение [Doc](../../loadformat/).

## Примеры



Показывает, как получить детали операции загрузки документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## См. также

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
