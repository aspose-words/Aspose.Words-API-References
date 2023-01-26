---
title: get_OleControl
second_title: Aspose.Words for C++ API Reference
description: Gets OleControl objects if this OLE object is an ActiveX control. Otherwise this property is null.
type: docs
weight: 79
url: /cpp/aspose.words.drawing/oleformat/get_olecontrol/
---
## OleFormat::get_OleControl method


Gets [OleControl](./) objects if this OLE object is an ActiveX control. Otherwise this property is null.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Ole::OleControl> Aspose::Words::Drawing::OleFormat::get_OleControl()
```


## Examples



Shows how to verify the properties of an ActiveX control. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"ActiveX controls.docx");

auto shape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));
SharedPtr<OleControl> oleControl = shape->get_OleFormat()->get_OleControl();

ASPOSE_ASSERT_EQ(nullptr, oleControl->get_Name());

if (oleControl->get_IsForms2OleControl())
{
    auto checkBox = System::DynamicCast<Forms2OleControl>(oleControl);
    ASSERT_EQ(u"Первый", checkBox->get_Caption());
    ASSERT_EQ(u"0", checkBox->get_Value());
    ASPOSE_ASSERT_EQ(true, checkBox->get_Enabled());
    ASSERT_EQ(Forms2OleControlType::CheckBox, checkBox->get_Type());
    ASPOSE_ASSERT_EQ(nullptr, checkBox->get_ChildNodes());
}
```

## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
