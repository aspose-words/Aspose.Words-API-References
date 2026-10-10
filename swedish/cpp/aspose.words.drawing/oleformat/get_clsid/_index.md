---
title: "Aspose::Words::Drawing::OleFormat::get_Clsid metod"
linktitle: "get_Clsid"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::OleFormat::get_Clsid metod. Hämtar CLSID för OLE‑objektet i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.drawing/oleformat/get_clsid/
---
## OleFormat::get_Clsid method


Hämtar CLSID för OLE-objektet.

```cpp
System::Guid Aspose::Words::Drawing::OleFormat::get_Clsid()
```


## Exempel



Visar hur man får åtkomst till en OLE‑kontroll som är inbäddad i ett dokument och dess underkontroller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE ActiveX controls.docm");

// Former lagrar och visar OLE‑objekt i dokumentets brödtext.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(u"6e182020-f460-11ce-9bcd-00aa00608e01", System::ObjectExt::ToString(shape->get_OleFormat()->get_Clsid()));

auto oleControl = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(shape->get_OleFormat()->get_OleControl());

// Vissa OLE‑kontroller kan innehålla underkontroller, till exempel den i detta dokument med tre alternativknappar.
System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControlCollection> oleControlCollection = oleControl->get_ChildNodes();

ASSERT_EQ(3, oleControlCollection->get_Count());

ASSERT_EQ(u"C#", oleControlCollection->idx_get(0)->get_Caption());
ASSERT_EQ(u"1", oleControlCollection->idx_get(0)->get_Value());

ASSERT_EQ(u"Visual Basic", oleControlCollection->idx_get(1)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(1)->get_Value());

ASSERT_EQ(u"Delphi", oleControlCollection->idx_get(2)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(2)->get_Value());
```

## Se även

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
