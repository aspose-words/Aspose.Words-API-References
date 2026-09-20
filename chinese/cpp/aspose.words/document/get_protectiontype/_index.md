---
title: "Aspose::Words::Document::get_ProtectionType 方法"
linktitle: "get_ProtectionType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_ProtectionType 方法。获取 C++ 中当前活动的文档保护类型。"
type: docs
weight: 44000
url: /zh/cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


获取当前活动的文档保护类型。

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## 备注


此属性允许检索当前设置的文档保护类型。要更改文档保护类型，请使用 [Protect()](../) 和 [Unprotect](../unprotect/) 方法。

当文档受到保护时，用户只能进行有限的更改，例如添加批注、进行修订或填写表单。

请注意，文档保护不同于写保护。写保护是通过 [WriteProtection](../get_writeprotection/) 指定的。

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
