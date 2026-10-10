---
title: "Aspose::Words::ProtectionType 枚举"
linktitle: "ProtectionType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ProtectionType 枚举。C++ 中文档的保护类型。"
type: docs
weight: 111000
url: /zh/cpp/aspose.words/protectiontype/
---
## ProtectionType enum


文档的保护类型。

```cpp
enum class ProtectionType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| AllowOnlyComments | 1 | 用户只能修改文档中的批注。 |
| AllowOnlyFormFields | 2 | 用户只能在文档的表单字段中输入数据。 |
| AllowOnlyRevisions | 0 | 用户只能向文档添加修订标记。 |
| ReadOnly | 3 | 文档不允许进行任何更改。自 Microsoft Word 2003 起可用。 |
| NoProtection | -1 | 文档未受保护。 |


## 示例



Shows how to turn off protection for a section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Apply write protection to every section in the document.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Turn off write protection for the first section.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// In this output document, we will be able to edit the first section freely,
// and we will only be able to edit the contents of the form field in the second section.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
