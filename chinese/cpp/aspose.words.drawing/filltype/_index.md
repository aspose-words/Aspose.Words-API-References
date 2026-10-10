---
title: "Aspose::Words::Drawing::FillType 枚举"
linktitle: "填充类型"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::FillType 枚举。指定 C++ 中可填充对象的填充类型。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.drawing/filltype/
---
## FillType enum


指定可填充对象的填充类型。

```cpp
enum class FillType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 实线 | 1 | 实心填充。 |
| 图案 | 2 | 图案填充。 |
| 渐变 | 3 | 渐变填充。 |
| 纹理化 | 4 | 纹理填充。 |
| Background | 5 | [Fill](../fill/) 与背景相同。 |
| Picture | 6 | 图片填充。 |


## 示例



展示如何将任意填充转换回实心填充。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// 获取第一个 Run 的字体的 Fill 对象。
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// 检查字体的 Fill 属性。
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// 将填充类型更改为实心，并使用统一的绿色颜色。
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
