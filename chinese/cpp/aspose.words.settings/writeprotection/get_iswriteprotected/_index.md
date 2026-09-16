---
title: "Aspose::Words::Settings::WriteProtection::get_IsWriteProtected 方法"
linktitle: "get_IsWriteProtected"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::WriteProtection::get_IsWriteProtected 方法。 当在 C++ 中设置了写保护密码时返回 true。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.settings/writeprotection/get_iswriteprotected/
---
## WriteProtection::get_IsWriteProtected method


当设置了写保护密码时返回 **true**。

```cpp
bool Aspose::Words::Settings::WriteProtection::get_IsWriteProtected()
```


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
