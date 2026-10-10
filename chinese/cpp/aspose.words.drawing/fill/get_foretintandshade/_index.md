---
title: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade 方法"
linktitle: "get_ForeTintAndShade"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade 方法。获取或设置一个 double 值，用于在 C++ 中调亮或调暗前景颜色。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


获取或设置用于调亮或调暗前景颜色的 double 值。

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## 备注


此属性的允许值范围为 -1（最暗）到 1（最亮）。

零 (0) 为中性。

## 示例



展示如何管理前景字体颜色的调亮和调暗。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::Drawing::Fill> textFill = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Fill();
textFill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
if (textFill->get_ForeTintAndShade() == 0)
{
    textFill->set_ForeTintAndShade(0.5);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillTintAndShade.docx");
```

## 另见

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
