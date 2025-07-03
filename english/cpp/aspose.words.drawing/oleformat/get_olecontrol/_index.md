---
title: Aspose::Words::Drawing::OleFormat::get_OleControl method
linktitle: get_OleControl
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OleFormat::get_OleControl method. Gets OleControl objects if this OLE object is an ActiveX control. Otherwise this property is null in C++.'
type: docs
weight: 7000
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
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"ActiveX controls.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Ole::OleControl> oleControl = shape->get_OleFormat()->get_OleControl();

ASSERT_EQ(u"CheckBox1", oleControl->get_Name());

if (oleControl->get_IsForms2OleControl())
{
    auto checkBox = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(oleControl);
    ASSERT_EQ(u"First", checkBox->get_Caption());
    ASSERT_EQ(u"0", checkBox->get_Value());
    ASPOSE_ASSERT_EQ(true, checkBox->get_Enabled());
    ASSERT_EQ(Aspose::Words::Drawing::Ole::Forms2OleControlType::CheckBox, checkBox->get_Type());
    ASPOSE_ASSERT_EQ(nullptr, checkBox->get_ChildNodes());
    ASSERT_EQ(System::String::Empty, checkBox->get_GroupName());

    // Note, that you can't set GroupName for a Frame.
    checkBox->set_GroupName(u"Aspose group name");
}
```

## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
