---
title: "Aspose::Words::Settings::WriteProtection::ValidatePassword 方法"
linktitle: "ValidatePassword"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::WriteProtection::ValidatePassword 方法。 如果指定的密码与文档所使用的写保护密码相同，则返回 true。如果文档未使用密码进行写保护，则在 C++ 中返回 false。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection::ValidatePassword method


如果指定的密码与文档受写保护时使用的密码相同，则返回 **true**。如果文档未使用密码进行写保护，则返回 **false**。

```cpp
bool Aspose::Words::Settings::WriteProtection::ValidatePassword(const System::String &password)
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
