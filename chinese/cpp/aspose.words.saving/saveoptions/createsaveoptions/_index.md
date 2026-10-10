---
title: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions 方法"
linktitle: "CreateSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions 方法。创建一个适用于指定保存格式的保存选项对象（类），在 C++ 中使用。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


创建一个适用于指定保存格式的保存选项对象。

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | 用于创建保存选项对象的保存格式。 |

### ReturnValue

一个从 [SaveOptions](../) 派生的类的对象。

## 另见

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


创建一个适用于给定文件名中指定的文件扩展名的保存选项对象。

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 此文件名的扩展名决定要创建的保存选项对象的类。 |

### ReturnValue

一个从 [SaveOptions](../) 派生的类的对象。

## 示例



展示如何为没有附加模板的文档设置默认模板。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 启用自动样式更新，但不附加模板文档。
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// 由于没有模板文档，文档无法跟踪样式更改。
// 使用 SaveOptions 对象自动设置模板
// 如果我们正在保存的文档没有模板。
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## 另见

* Class [SaveOptions](../)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
