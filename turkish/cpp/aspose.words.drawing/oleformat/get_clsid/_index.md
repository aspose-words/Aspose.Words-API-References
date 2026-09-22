---
title: "Aspose::Words::Drawing::OleFormat::get_Clsid yöntemi"
linktitle: "get_Clsid"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::OleFormat::get_Clsid yöntemi. OLE nesnesinin CLSID'sini C++'ta alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing/oleformat/get_clsid/
---
## OleFormat::get_Clsid method


OLE nesnesinin CLSID'sini alır.

```cpp
System::Guid Aspose::Words::Drawing::OleFormat::get_Clsid()
```


## Örnekler



Bir belgede gömülü OLE denetimine ve onun alt denetimlerine nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE ActiveX controls.docm");

// Şekiller, belgenin gövdesinde OLE nesnelerini depolar ve gösterir.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(u"6e182020-f460-11ce-9bcd-00aa00608e01", System::ObjectExt::ToString(shape->get_OleFormat()->get_Clsid()));

auto oleControl = System::ExplicitCast<Aspose::Words::Drawing::Ole::Forms2OleControl>(shape->get_OleFormat()->get_OleControl());

// Bazı OLE denetimleri, bu belgede üç seçenek düğmesi bulunan gibi, alt denetimler içerebilir.
System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControlCollection> oleControlCollection = oleControl->get_ChildNodes();

ASSERT_EQ(3, oleControlCollection->get_Count());

ASSERT_EQ(u"C#", oleControlCollection->idx_get(0)->get_Caption());
ASSERT_EQ(u"1", oleControlCollection->idx_get(0)->get_Value());

ASSERT_EQ(u"Visual Basic", oleControlCollection->idx_get(1)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(1)->get_Value());

ASSERT_EQ(u"Delphi", oleControlCollection->idx_get(2)->get_Caption());
ASSERT_EQ(u"0", oleControlCollection->idx_get(2)->get_Value());
```

## Ayrıca Bakınız

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
