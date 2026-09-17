---
title: "Aspose::Words::Drawing::OleFormat::get_Clsid méthode"
linktitle: "get_Clsid"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::OleFormat::get_Clsid méthode. Obtient le CLSID de l'objet OLE en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.drawing/oleformat/get_clsid/
---
## OleFormat::get_Clsid method


Obtient le CLSID de l'objet OLE.

```cpp
System::Guid Aspose::Words::Drawing::OleFormat::get_Clsid()
```


## Exemples



Montre comment accéder à un contrôle OLE incorporé dans un document et à ses contrôles enfants.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE ActiveX controls.docm");

// Les formes stockent et affichent les objets OLE dans le corps du document.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(u"6e182020-f460-11ce-9bcd-00aa00608e01", System::ObjectExt::ToString(shape->get_OleFormat()->get_Clsid()));

auto oleControl = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(shape->get_OleFormat()->get_OleControl());

// Certains contrôles OLE peuvent contenir des contrôles enfants, comme celui de ce document avec trois boutons d'options.
System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControlCollection> oleControlCollection = oleControl->get_ChildNodes();

ASSERT_EQ(3, oleControlCollection->get_Count());

ASSERT_EQ(u"C#", oleControlCollection->idx_get(0)->get_Caption());
ASSERT_EQ(u"1", oleControlCollection->idx_get(0)->get_Value());

ASSERT_EQ(u"Visual Basic", oleControlCollection->idx_get(1)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(1)->get_Value());

ASSERT_EQ(u"Delphi", oleControlCollection->idx_get(2)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(2)->get_Value());
```

## Voir aussi

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
