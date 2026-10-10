---
title: "Aspose::Words::Fields::FieldEQ::AsOfficeMath 方法"
linktitle: "AsOfficeMath"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldEQ::AsOfficeMath 方法。返回与 EQ 字段对应的 Office Math 对象（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


返回与 EQ 字段对应的 Office [Math](../../../aspose.words.math/) 对象。

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

如果字段代码为空或无效，则返回 **null**，否则返回一个 [OfficeMath](../../../aspose.words.math/officemath/) 实例。

## 示例



展示如何使用 Office [Math](../../../aspose.words.math/) 替换 EQ 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## 另见

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
