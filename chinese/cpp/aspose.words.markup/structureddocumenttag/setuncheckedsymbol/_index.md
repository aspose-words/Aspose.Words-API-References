---
title: "Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol method"
linktitle: "SetUncheckedSymbol"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol method. 设置用于表示复选框内容控件未选中状态的符号（C++ 中）。"
type: docs
weight: 59000
url: /zh/cpp/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag::SetUncheckedSymbol method


设置用于表示复选框内容控件未选状态的符号。

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol(int32_t characterCode, const System::String &fontName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| characterCode | int32_t | 指定符号的字符代码。 |
| fontName | const System::String\& | 包含该符号的字体名称。 |
## 备注


访问此方法仅适用于 [Checkbox](../../sdttype/) SDT 类型。

对于所有其他 SDT 类型，将会出现异常。

## 示例



展示如何以复选框形式创建结构化文档标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// 我们可以设置用于表示复选框内容控件已选/未选状态的符号。
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## 另见

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
