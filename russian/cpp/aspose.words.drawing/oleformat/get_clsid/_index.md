---
title: "Aspose::Words::Drawing::OleFormat::get_Clsid метод"
linktitle: "get_Clsid"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::OleFormat::get_Clsid метод. Получает CLSID OLE‑объекта в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing/oleformat/get_clsid/
---
## OleFormat::get_Clsid method


Получает CLSID OLE-объекта.

```cpp
System::Guid Aspose::Words::Drawing::OleFormat::get_Clsid()
```


## Примеры



Показывает, как получить доступ к OLE‑элементу, внедрённому в документ, и его дочерним элементам.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE ActiveX controls.docm");

// Фигуры хранят и отображают OLE‑объекты в теле документа.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(u"6e182020-f460-11ce-9bcd-00aa00608e01", System::ObjectExt::ToString(shape->get_OleFormat()->get_Clsid()));

auto oleControl = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(shape->get_OleFormat()->get_OleControl());

// Некоторые OLE‑элементы могут содержать дочерние элементы, например тот, который находится в этом документе и имеет три переключателя.
System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControlCollection> oleControlCollection = oleControl->get_ChildNodes();

ASSERT_EQ(3, oleControlCollection->get_Count());

ASSERT_EQ(u"C#", oleControlCollection->idx_get(0)->get_Caption());
ASSERT_EQ(u"1", oleControlCollection->idx_get(0)->get_Value());

ASSERT_EQ(u"Visual Basic", oleControlCollection->idx_get(1)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(1)->get_Value());

ASSERT_EQ(u"Delphi", oleControlCollection->idx_get(2)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(2)->get_Value());
```

## См. также

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
