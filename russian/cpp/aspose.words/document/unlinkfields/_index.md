---
title: "Aspose::Words::Document::UnlinkFields метод"
linktitle: "UnlinkFields"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::UnlinkFields метод. Отсоединяет поля во всём документе в C++."
type: docs
weight: 94000
url: /ru/cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


Отвязывает поля во всём документе.

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## Примечания


Заменяет все поля во всём документе их последними результатами.

Чтобы отсоединить поля в определённой части документа, используйте [UnlinkFields](../../range/unlinkfields/).

## Примеры



Показывает, как отсоединить все поля в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

doc->UnlinkFields();
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
