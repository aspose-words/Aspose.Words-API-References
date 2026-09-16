---
title: "Aspose::Words::Drawing::OleFormat::GetRawData 方法"
linktitle: "GetRawData"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::OleFormat::GetRawData 方法。获取 OLE 对象的原始数据（在 C++ 中）。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat::GetRawData method


获取 OLE 对象的原始数据。

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::OleFormat::GetRawData()
```


## 示例



展示如何访问嵌入式 OLE 对象的原始数据。
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

## 另见

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
