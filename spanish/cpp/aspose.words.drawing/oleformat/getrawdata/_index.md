---
title: "Aspose::Words::Drawing::OleFormat::GetRawData método"
linktitle: "GetRawData"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::OleFormat::GetRawData método. Obtiene los datos sin procesar del objeto OLE en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat::GetRawData method


Obtiene los datos sin procesar del objeto OLE.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::OleFormat::GetRawData()
```


## Ejemplos



Muestra cómo acceder a los datos sin procesar de un objeto OLE incrustado.
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

## Ver también

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
