---
title: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath 方法"
linktitle: "get_ConvertShapeToOfficeMath"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath 方法。获取或设置是否在 C++ 中将带有 EquationXML 的形状转换为 Office Math 对象。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


获取或设置是否将带有 EquationXML 的形状转换为 Office [Math](../../../aspose.words.math/) 对象。

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## 示例



展示如何将 EquationXML 形状转换为 Office [Math](../../../aspose.words.math/) 对象。
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// 使用此标志指定是否转换带有 EquationXML 属性的形状
// 为 Office Math 对象，然后加载文档。
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

## 另见

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
