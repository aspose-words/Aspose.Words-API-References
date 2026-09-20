---
title: "метод Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath"
linktitle: "get_ConvertShapeToOfficeMath"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath. Получает или задает, следует ли преобразовывать фигуры с EquationXML в объекты Office Math в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


Получает или задает, следует ли преобразовывать фигуры с EquationXML в объекты Office [Math](../../../aspose.words.math/).

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## Примеры



Показывает, как преобразовать фигуры EquationXML в объекты Office [Math](../../../aspose.words.math/).
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// Используйте этот флаг, чтобы указать, следует ли преобразовывать фигуры с атрибутами EquationXML
// в объекты Office Math, а затем загрузить документ.
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

## См. также

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
