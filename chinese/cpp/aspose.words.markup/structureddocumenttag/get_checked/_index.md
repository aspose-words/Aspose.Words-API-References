---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Checked 方法"
linktitle: "get_Checked"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Checked 方法。获取/设置复选框 SDT 的当前状态。此属性在 C++ 中的默认值为 false。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag::get_Checked method


获取/设置复选框 **SDT** 的当前状态。此属性的默认值为 **false**。

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```

## 备注


访问此属性仅适用于 [Checkbox](../../sdttype/) SDT 类型。

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
