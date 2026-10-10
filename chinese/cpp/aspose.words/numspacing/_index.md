---
title: "Aspose::Words::NumSpacing enum"
linktitle: "NumSpacing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NumSpacing 枚举。指定在 C++ 中数字间距可以显示的可能取值。"
type: docs
weight: 103500
url: /zh/cpp/aspose.words/numspacing/
---
## NumSpacing enum


指定数字间距可以显示的可能值。

```cpp
enum class NumSpacing
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Default | 0 | 指定数字以字体的默认形式显示。 |
| 比例 | 1 | 指定如果字体支持，则以比例间距设计的数字形式显示。 |
| 等宽 | 2 | 指定如果字体支持，则以等宽设计的数字形式显示。 |


## 示例



展示如何设置数字的间距类型。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 此效果仅在较新版本的 MS Word 中受支持。
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
