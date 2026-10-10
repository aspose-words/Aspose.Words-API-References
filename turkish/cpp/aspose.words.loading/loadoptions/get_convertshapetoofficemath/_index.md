---
title: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath metodu"
linktitle: "get_ConvertShapeToOfficeMath"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath metodu. C++'ta şekilleri EquationXML ile Office Math nesnelerine dönüştürüp dönüştürmeyeceğini alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


Şekilleri EquationXML ile Office [Math](../../../aspose.words.math/) nesnelerine dönüştürüp dönüştürmeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## Örnekler



EquationXML şekillerinin Office [Math](../../../aspose.words.math/) nesnelerine nasıl dönüştürüleceğini gösterir.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// Bu bayrağı, EquationXML öznitelikleriyle şekilleri dönüştürüp dönüştürmeyeceğinizi belirtmek için kullanın
// Office Math nesnelerine dönüştürmek ve ardından belgeyi yüklemek için.
loadOptions->set_ConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    ASSERT_EQ(16, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
    ASSERT_EQ(34, doc->GetChildNodes(Aspose::Words::NodeType::OfficeMath, true)->get_Count());
}
else
{
    ASSERT_EQ(24, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
    ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::OfficeMath, true)->get_Count());
}
```

## Ayrıca Bakınız

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
