---
title: "Aspose::Words::Settings::WriteProtection::SetPassword 方法"
linktitle: "SetPassword"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::WriteProtection::SetPassword 方法。设置文档的写保护密码（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection::SetPassword method


设置文档的写保护密码。

```cpp
void Aspose::Words::Settings::WriteProtection::SetPassword(const System::String &password)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 密码 | const System::String\& | 要设置的密码。不能为 **null**，但可以是空字符串。 |
## 备注


如果设置了密码，Microsoft Word 将要求用户输入密码或以只读方式打开文档。

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

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
