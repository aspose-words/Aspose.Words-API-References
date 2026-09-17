---
title: "Méthode Aspose::Words::Drawing::OleFormat::GetRawData"
linktitle: "GetRawData"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::OleFormat::GetRawData. Obtient les données brutes de l'objet OLE en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat::GetRawData method


Obtient les données brutes de l'objet OLE.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::OleFormat::GetRawData()
```


## Exemples



Montre comment accéder aux données brutes d'un objet OLE intégré.
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

## Voir aussi

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
