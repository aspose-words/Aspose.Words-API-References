---
title: "Aspose::Words::Drawing::OleFormat::get_OleControl método"
linktitle: "get_OleControl"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::OleFormat::get_OleControl método. Obtiene objetos OleControl si este objeto OLE es un control ActiveX. De lo contrario, esta propiedad es nula en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.drawing/oleformat/get_olecontrol/
---
## OleFormat::get_OleControl method


Obtiene objetos [OleControl](./) si este objeto OLE es un control ActiveX. De lo contrario, esta propiedad es nula.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Ole::OleControl> Aspose::Words::Drawing::OleFormat::get_OleControl()
```


## Ejemplos



Muestra cómo verificar las propiedades de un control ActiveX.
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

    // Nota, no puedes establecer GroupName para un Frame.
    checkBox->set_GroupName(u"Aspose group name");
}
```

## Ver también

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
