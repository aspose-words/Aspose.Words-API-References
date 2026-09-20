---
title: "Метод Aspose::Words::Range::UnlinkFields"
linktitle: "UnlinkFields"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Range::UnlinkFields. Отсоединяет поля в этом диапазоне в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words/range/unlinkfields/
---
## Range::UnlinkFields method


Отсоединяет поля в этом диапазоне.

```cpp
void Aspose::Words::Range::UnlinkFields()
```

## Примечания


Заменяет все поля в этом диапазоне их последними результатами.

Чтобы отсоединить поля во всём документе, используйте [UnlinkFields](./).

## Примеры



Показывает, как отсоединить все поля в диапазоне.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

auto newSection = System::ExplicitCast<Aspose::Words::Section>(System::ExplicitCast<Aspose::Words::Node>(doc->get_Sections()->idx_get(0))->Clone(true));
doc->get_Sections()->Add(newSection);

doc->get_Sections()->idx_get(1)->get_Range()->UnlinkFields();
```

## См. также

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
