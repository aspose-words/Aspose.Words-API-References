---
title: "Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended 方法"
linktitle: "get_ReadOnlyRecommended"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended 方法。指定文档作者是否建议在 C++ 中将文档以只读方式打开。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.settings/writeprotection/get_readonlyrecommended/
---
## WriteProtection::get_ReadOnlyRecommended method


指定文档作者是否建议将文档以只读方式打开。

```cpp
bool Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended() const
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
