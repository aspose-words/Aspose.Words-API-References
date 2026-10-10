---
title: "Aspose::Words::Drawing::OleFormat::get_OleControl metod"
linktitle: "get_OleControl"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::OleFormat::get_OleControl metod. Hämtar OleControl‑objekt om detta OLE‑objekt är en ActiveX‑kontroll. Annars är denna egenskap null i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.drawing/oleformat/get_olecontrol/
---
## OleFormat::get_OleControl method


Hämtar [OleControl](./)-objekt om detta OLE-objekt är en ActiveX-kontroll. Annars är denna egenskap null.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Ole::OleControl> Aspose::Words::Drawing::OleFormat::get_OleControl()
```


## Exempel



Visar hur man verifierar egenskaperna för en ActiveX-kontroll.
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

    // Observera att du inte kan ange GroupName för en Frame.
    checkBox->set_GroupName(u"Aspose group name");
}
```

## Se även

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
