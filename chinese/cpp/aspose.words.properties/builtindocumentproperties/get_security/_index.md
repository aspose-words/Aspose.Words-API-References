---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security 方法"
linktitle: "get_Security"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security 方法。指定文档的安全级别，以数值形式表示（C++）。"
type: docs
weight: 25000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_security/
---
## BuiltInDocumentProperties::get_Security method


指定文档的安全级别（数值）。

```cpp
Aspose::Words::Properties::DocumentSecurity Aspose::Words::Properties::BuiltInDocumentProperties::get_Security()
```

## 备注


仅将此属性用于信息目的，因为 Microsoft Word 并不总是设置此属性。此属性仅在 DOC 和 OOXML 文档中可用。

要保护或取消保护文档，请使用 [Protect()](../) 和 [Unprotect](../../../aspose.words/document/unprotect/) 方法。

Aspose.Words 在保存文档之前会将此属性更新为正确的值。

## 示例



展示如何使用文档属性显示文档的安全级别。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// 如果我们将文档配置为只读，它将使用内置属性 "Security" 显示此状态。
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// 对文档进行写保护，然后验证其安全级别。
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// "Security" 是描述性属性。我们可以手动编辑其值。
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## 另见

* Enum [DocumentSecurity](../../documentsecurity/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
