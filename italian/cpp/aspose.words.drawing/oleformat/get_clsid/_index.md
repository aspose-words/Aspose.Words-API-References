---
title: "Aspose::Words::Drawing::OleFormat::get_Clsid metodo"
linktitle: "get_Clsid"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::OleFormat::get_Clsid metodo. Ottiene il CLSID dell'oggetto OLE in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing/oleformat/get_clsid/
---
## OleFormat::get_Clsid method


Ottiene il CLSID dell'oggetto OLE.

```cpp
System::Guid Aspose::Words::Drawing::OleFormat::get_Clsid()
```


## Esempi



Mostra come accedere a un controllo OLE incorporato in un documento e ai suoi controlli figli.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE ActiveX controls.docm");

// Le forme memorizzano e visualizzano gli oggetti OLE nel corpo del documento.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(u"6e182020-f460-11ce-9bcd-00aa00608e01", System::ObjectExt::ToString(shape->get_OleFormat()->get_Clsid()));

auto oleControl = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(shape->get_OleFormat()->get_OleControl());

// Alcuni controlli OLE possono contenere controlli figli, come quello in questo documento con tre pulsanti di opzione.
System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControlCollection> oleControlCollection = oleControl->get_ChildNodes();

ASSERT_EQ(3, oleControlCollection->get_Count());

ASSERT_EQ(u"C#", oleControlCollection->idx_get(0)->get_Caption());
ASSERT_EQ(u"1", oleControlCollection->idx_get(0)->get_Value());

ASSERT_EQ(u"Visual Basic", oleControlCollection->idx_get(1)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(1)->get_Value());

ASSERT_EQ(u"Delphi", oleControlCollection->idx_get(2)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(2)->get_Value());
```

## Vedi anche

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
