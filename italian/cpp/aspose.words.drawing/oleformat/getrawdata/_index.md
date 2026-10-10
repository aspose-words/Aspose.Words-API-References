---
title: "Aspose::Words::Drawing::OleFormat::GetRawData method"
linktitle: "GetRawData"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::OleFormat::GetRawData method. Ottiene i dati grezzi dell'oggetto OLE in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat::GetRawData method


Ottiene i dati grezzi dell'oggetto OLE.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::OleFormat::GetRawData()
```


## Esempi



Mostra come accedere ai dati grezzi di un oggetto OLE incorporato.
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

## Vedi anche

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
