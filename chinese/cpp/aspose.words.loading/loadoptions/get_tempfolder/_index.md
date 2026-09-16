---
title: "Aspose::Words::Loading::LoadOptions::get_TempFolder 方法"
linktitle: "get_TempFolder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_TempFolder 方法。允许在读取文档时使用临时文件。默认情况下此属性为 null，C++ 中不使用临时文件。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


允许在读取文档时使用临时文件。默认情况下此属性为 **null**，不使用临时文件。

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## 备注


文件夹必须存在且可写，否则将抛出异常。

Aspose.Words 在读取完成后会自动删除所有临时文件。

## 示例



展示如何使用临时文件加载文档。
```cpp
// 请注意，此方法可以降低内存使用，但会降低速度
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// 确保目录存在并加载
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);
```


展示在加载文档时如何使用硬盘而非内存。
```cpp
// 当我们加载文档时，各种元素会在保存操作期间临时存储在内存中。
// 我们可以使用此选项改为在本地文件系统中使用临时文件夹，
// 这将减少我们应用程序的内存开销。
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// 指定的临时文件夹必须在加载操作之前存在于本地文件系统中。
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", options);

// 该文件夹将在加载操作后保持存在且不含残留内容。
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## 另见

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
