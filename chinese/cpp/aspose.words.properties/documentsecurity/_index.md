---
title: "Aspose::Words::Properties::DocumentSecurity enum"
linktitle: "DocumentSecurity"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentSecurity enum. 用作 Security 属性的值。指定文档的安全级别为 C++ 中的数值。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


用作 [Security](../builtindocumentproperties/get_security/) 属性的值。指定文档的安全级别为数值。

```cpp
enum class DocumentSecurity
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 该属性未指定任何安全状态。 |
| PasswordProtected | 1 | 该文档受密码保护。（注意，迄今为止在文档中从未见过此情况）。 |
| ReadOnlyRecommended | 2 | 文档将在可能的情况下以只读方式打开，但此设置可以被覆盖。 |
| ReadOnlyEnforced | 4 | 文档将始终以只读方式打开。 |
| ReadOnlyExceptAnnotations | 8 | 文档将始终以只读方式打开，但注释除外。 |


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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
