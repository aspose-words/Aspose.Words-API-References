---
title: "Aspose::Words::Settings::WriteProtection 类"
linktitle: "WriteProtection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::WriteProtection 类。指定文档的写保护设置。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


指定文档的写保护设置。欲了解更多，请访问 [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/) 文档文章。

```cpp
class WriteProtection : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | 当设置了写保护密码时返回 **true**。 |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | 指定文档作者是否建议将文档以只读方式打开。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | 用于设置 [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/) 的 setter。 |
| [SetPassword](./setpassword/)(const System::String\&) | 设置文档的写保护密码。 |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | 如果指定的密码与文档受写保护时使用的密码相同，则返回 **true**。如果文档未使用密码进行写保护，则返回 **false**。 |
## 备注


写保护指定作者是否建议将文档以只读方式打开和/或需要密码才能修改文档。

写保护不同于文档保护。写保护在 Microsoft Word 的“另存为”对话框选项中进行设置。

您不能直接创建此类的实例。您可以通过 [WriteProtection](../../aspose.words/document/get_writeprotection/) 属性访问文档保护设置。

## 示例



展示如何使用密码保护文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// 输入长度不超过 15 个字符的密码，然后验证文档的保护状态。
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// 保护不会阻止程序化编辑文档，也不会加密内容。
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
