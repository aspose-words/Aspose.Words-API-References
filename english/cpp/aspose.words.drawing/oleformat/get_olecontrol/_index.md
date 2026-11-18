---
title: Aspose::Words::Drawing::OleFormat::get_OleControl method
linktitle: get_OleControl
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OleFormat::get_OleControl method. Gets OleControl objects if this OLE object is an ActiveX control. Otherwise this property is null in C++.'
type: docs
weight: 19432
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
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"ActiveX controls.docx"));

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Ole::OleControl> oleControl = shape->get_OleFormat()->get_OleControl();

ASSERT_EQ(oleControl->get_Name(), u"CheckBox1");

if (oleControl->get_IsForms2OleControl())
{
    auto checkBox = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(oleControl);
    ASSERT_EQ(checkBox->get_Caption(), u"First");
    ASSERT_EQ(checkBox->get_Value(), u"0");
    ASPOSE_ASSERT_EQ(checkBox->get_Enabled(), true);
    ASSERT_EQ(checkBox->get_Type(), Forms2OleControlType::CheckBox);
    ASPOSE_ASSERT_EQ(checkBox->get_ChildNodes(), nullptr);
    ASSERT_EQ(checkBox->get_GroupName(), System::String::Empty);

    // Note, that you can't set GroupName for a Frame.
    checkBox->set_GroupName(u"Aspose group name");
}
```
## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
