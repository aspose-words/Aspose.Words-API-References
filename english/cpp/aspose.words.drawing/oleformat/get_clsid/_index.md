---
title: Aspose::Words::Drawing::OleFormat::get_Clsid method
linktitle: get_Clsid
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OleFormat::get_Clsid method. Gets the CLSID of the OLE object in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.drawing/oleformat/get_clsid/
---
## OleFormat::get_Clsid method


Gets the CLSID of the OLE object.

```cpp
System::Guid Aspose::Words::Drawing::OleFormat::get_Clsid()
```


## Examples



Shows how to access an OLE control embedded in a document and its child controls. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE ActiveX controls.docm");

// Shapes store and display OLE objects in the document's body.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(u"6e182020-f460-11ce-9bcd-00aa00608e01", System::ObjectExt::ToString(shape->get_OleFormat()->get_Clsid()));

auto oleControl = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(shape->get_OleFormat()->get_OleControl());

// Some OLE controls may contain child controls, such as the one in this document with three options buttons.
System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControlCollection> oleControlCollection = oleControl->get_ChildNodes();

ASSERT_EQ(3, oleControlCollection->get_Count());

ASSERT_EQ(u"C#", oleControlCollection->idx_get(0)->get_Caption());
ASSERT_EQ(u"1", oleControlCollection->idx_get(0)->get_Value());

ASSERT_EQ(u"Visual Basic", oleControlCollection->idx_get(1)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(1)->get_Value());

ASSERT_EQ(u"Delphi", oleControlCollection->idx_get(2)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(2)->get_Value());
```

## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
