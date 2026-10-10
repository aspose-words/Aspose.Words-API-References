---
title: "Aspose::Words::Document::Unprotect 方法"
linktitle: "Unprotect"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::Unprotect 方法。无论密码如何，均可从文档中移除保护（C++）。"
type: docs
weight: 95000
url: /zh/cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


无论密码如何，都移除文档的保护。

```cpp
void Aspose::Words::Document::Unprotect()
```

## 备注


即使文档设置了保护密码，此方法也会取消文档的保护。

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


如果指定了正确的密码，则移除文档的保护。

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 密码 | const System::String\& | 用于解除文档保护的密码。 |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## 备注


此方法仅在指定正确密码时才会解除文档的保护。

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
