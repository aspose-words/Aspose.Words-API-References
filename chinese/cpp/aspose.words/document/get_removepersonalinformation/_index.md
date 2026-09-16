---
title: "Aspose::Words::Document::get_RemovePersonalInformation 方法"
linktitle: "get_RemovePersonalInformation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_RemovePersonalInformation 方法。获取或设置一个标志，指示 Microsoft Word 在 C++ 中保存文档时将从注释、修订和文档属性中删除所有用户信息。"
type: docs
weight: 45000
url: /zh/cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


获取或设置一个标志，指示 Microsoft Word 在保存文档时将删除评论、修订和文档属性中的所有用户信息。

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## 示例



展示如何在手动保存时启用删除个人信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一些包含个人信息的内容。
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// 此标志等同于 File -> Options -> Trust Center -> Trust Center Settings... ->
// 隐私选项 -> "在保存时从文件属性中删除个人信息" 在 Microsoft Word 中。
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// 此选项在使用 Aspose.Words 执行的保存操作期间不会生效。
// 当我们使用 Microsoft Word 手动保存时，设置该标志后个人数据将从我们的文档中被删除。
doc->Save(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
