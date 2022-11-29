---
title: GetRawData
second_title: Aspose.Words for C++ API Reference
description: Gets OLE object raw data.
type: docs
weight: 183
url: /cpp/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat::GetRawData method


Gets OLE object raw data.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::OleFormat::GetRawData()
```


## Examples



Shows how to access the raw data of an embedded OLE object. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"OLE objects.docx");

for (const auto& shape : System::IterateOver(doc->GetChildNodes(NodeType::Shape, true)))
{
    SharedPtr<OleFormat> oleFormat = (System::DynamicCast<Shape>(shape))->get_OleFormat();
    if (oleFormat != nullptr)
    {
        std::cout << "This is " << (oleFormat->get_IsLink() ? String(u"a linked") : String(u"an embedded")) << " object" << std::endl;
        ArrayPtr<uint8_t> oleRawData = oleFormat->GetRawData();

        ASSERT_EQ(24576, oleRawData->get_Length());
    }
}
```

## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
