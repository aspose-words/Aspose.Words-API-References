---
title: "Aspose::Words::Drawing::OleFormat::get_ProgId метод"
linktitle: "get_ProgId"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::OleFormat::get_ProgId метод. Получает или задает ProgID объекта OLE в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.drawing/oleformat/get_progid/
---
## OleFormat::get_ProgId method


Получает или задает ProgID OLE-объекта.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_ProgId()
```

## Примечания


Свойство ProgID не всегда присутствует в документах Microsoft Word и на него нельзя полагаться.

Не может быть **null**.

Значение по умолчанию — пустая строка.

## Примеры



Показывает, как извлекать встроенные OLE‑объекты в файлы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// OLE‑объект в первой фигуре представляет собой таблицу Microsoft Excel.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Наш объект не обновляется автоматически и не заблокирован от обновлений.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Если мы планируем сохранять OLE‑объект в файл в локальной файловой системе,
// мы можем использовать свойство "SuggestedExtension", чтобы определить, какое расширение файла применить.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Ниже представлены два способа сохранения OLE‑объекта в файл в локальной файловой системе.
// 1 -  Сохранить через поток:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Сохранить напрямую в файл:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## См. также

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
