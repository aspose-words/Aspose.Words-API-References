---
title: "Aspose::Words::Drawing::OleFormat::get_Clsid-Methode"
linktitle: "get_Clsid"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::OleFormat::get_Clsid-Methode. Gibt die CLSID des OLE-Objekts in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words.drawing/oleformat/get_clsid/
---
## OleFormat::get_Clsid method


Liest die CLSID des OLE-Objekts.

```cpp
System::Guid Aspose::Words::Drawing::OleFormat::get_Clsid()
```


## Beispiele



Zeigt, wie man auf ein in einem Dokument eingebettetes OLE-Steuerelement und dessen untergeordnete Steuerelemente zugreift.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE ActiveX controls.docm");

// Formen speichern und zeigen OLE-Objekte im Dokumentkörper an.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(u"6e182020-f460-11ce-9bcd-00aa00608e01", System::ObjectExt::ToString(shape->get_OleFormat()->get_Clsid()));

auto oleControl = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(shape->get_OleFormat()->get_OleControl());

// Einige OLE-Steuerelemente können untergeordnete Steuerelemente enthalten, wie das in diesem Dokument mit drei Optionsschaltern.
System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControlCollection> oleControlCollection = oleControl->get_ChildNodes();

ASSERT_EQ(3, oleControlCollection->get_Count());

ASSERT_EQ(u"C#", oleControlCollection->idx_get(0)->get_Caption());
ASSERT_EQ(u"1", oleControlCollection->idx_get(0)->get_Value());

ASSERT_EQ(u"Visual Basic", oleControlCollection->idx_get(1)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(1)->get_Value());

ASSERT_EQ(u"Delphi", oleControlCollection->idx_get(2)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(2)->get_Value());
```

## Siehe auch

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
