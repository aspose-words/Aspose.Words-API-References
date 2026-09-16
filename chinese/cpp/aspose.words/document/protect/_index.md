---
title: "Aspose::Words::Document::Protect 方法"
linktitle: "保护"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::Protect 方法。保护文档不被更改，且不更改现有密码，或在 C++ 中分配一个随机密码。"
type: docs
weight: 67000
url: /zh/cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


在不更改现有密码的情况下保护文档免受更改，或分配一个随机密码。

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 类型 | Aspose::Words::ProtectionType | 指定文档的保护类型。 |
## 备注


当文档受到保护时，用户只能进行有限的更改，例如添加批注、进行修订或填写表单。

当您保护文档且该文档已经设置了保护密码时，现有的保护密码不会被更改。

当您保护文档且该文档没有保护密码时，此方法会分配一个随机密码，使得在 Microsoft Word 中无法取消保护该文档，但在 Aspose.Words 中仍可取消保护，因为取消保护时不需要密码。

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

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


保护文档免受更改，并可选地设置保护密码。

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 类型 | Aspose::Words::ProtectionType | 指定文档的保护类型。 |
| 密码 | const System::String\& | 用于保护文档的密码。如果希望在没有密码的情况下保护文档，请指定 **null** 或空字符串。 |
## 备注


当文档受到保护时，用户只能进行有限的更改，例如添加批注、进行修订或填写表单。

请注意，文档保护不同于写保护。写保护是使用 [WriteProtection](../get_writeprotection/) 指定的。

## 示例



展示如何保护和取消保护文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 如果我们使用 Microsoft Word 打开此文档并打算编辑它，
// 我们需要输入密码才能通过保护。
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// 请注意，此保护仅适用于使用 Microsoft Word 打开的用户。
// 我们并未以任何方式加密文档，且在程序中打开和编辑它时不需要密码。
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// 有两种方法可以解除文档的保护。
// 1 - 不使用密码：
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - 使用正确的密码：
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## 另见

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
