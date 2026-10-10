---
title: "Aspose::Words::Section::get_ProtectedForForms 方法"
linktitle: "get_ProtectedForForms"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Section::get_ProtectedForForms 方法。如果该节受表单保护，则返回 true。当节受表单保护时，用户只能在 Microsoft Word（C++ 中）中的表单字段中选择和修改文本。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


如果节已对表单受保护则为 True。当节对表单受保护时，用户只能在 Microsoft Word 中的表单字段中选择和修改文本。

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


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

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
