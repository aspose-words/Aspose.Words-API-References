---
title: "Aspose::Words::Drawing::Fill::get_Color 方法"
linktitle: "get_Color"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill::get_Color 方法。获取或设置表示填充前景颜色的 Color 对象（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.drawing/fill/get_color/
---
## Fill::get_Color method


获取或设置表示填充前景颜色的 Color 对象。

```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_Color()
```


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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
