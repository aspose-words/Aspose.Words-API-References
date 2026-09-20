---
title: "Aspose::Words::Fields::Field::Unlink метод"
linktitle: "Отсоединить"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::Field::Unlink метод. Выполняет разъединение поля в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.fields/field/unlink/
---
## Field::Unlink method


Выполняет отсоединение поля.

```cpp
bool Aspose::Words::Fields::Field::Unlink()
```


### ReturnValue

**true** if the field has been unlinked, otherwise **false**.
## Примечания


Заменяет поле его последним результатом.

Некоторые поля, такие как поля XE (Index Entry) и поля SEQ (Sequence), нельзя отсоединить.

## Примеры



Показывает, как отсоединить поле.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");
doc->get_Range()->get_Fields()->idx_get(1)->Unlink();
```

## См. также

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
