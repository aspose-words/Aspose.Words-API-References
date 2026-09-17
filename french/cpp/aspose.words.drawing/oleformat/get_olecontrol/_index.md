---
title: "Aspose::Words::Drawing::OleFormat::get_OleControl méthode"
linktitle: "get_OleControl"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::OleFormat::get_OleControl méthode. Obtient des objets OleControl si cet objet OLE est un contrôle ActiveX. Sinon, cette propriété est nulle en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.drawing/oleformat/get_olecontrol/
---
## OleFormat::get_OleControl method


Obtient des objets [OleControl](./) si cet objet OLE est un contrôle ActiveX. Sinon, cette propriété est nulle.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Ole::OleControl> Aspose::Words::Drawing::OleFormat::get_OleControl()
```


## Exemples



Montre comment vérifier les propriétés d'un contrôle ActiveX.
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

    // Notez que vous ne pouvez pas définir GroupName pour un Frame.
    checkBox->set_GroupName(u"Aspose group name");
}
```

## Voir aussi

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
