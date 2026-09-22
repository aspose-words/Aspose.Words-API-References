---
title: "Aspose::Words::Drawing::OleFormat::GetRawData yöntemi"
linktitle: "GetRawData"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::OleFormat::GetRawData yöntemi. C++'de OLE nesnesinin ham verisini alır."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat::GetRawData method


OLE nesnesi ham verisini alır.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::OleFormat::GetRawData()
```


## Örnekler



Gömülü bir OLE nesnesinin ham verisine nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx");

for (auto&& shape : System::IterateOver<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)))
{
    System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();
    if (oleFormat != nullptr)
    {
        std::cout << System::String::Format(u"This is {0} object", (oleFormat->get_IsLink() ? System::String(u"a linked") : System::String(u"an embedded"))) << std::endl;
        System::ArrayPtr<uint8_t> oleRawData = oleFormat->GetRawData();

        ASSERT_EQ(24576, oleRawData->get_Length());
    }
}
```

## Ayrıca Bakınız

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
