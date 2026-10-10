---
title: "Aspose::Words::Saving::SaveOptions::get_TempFolder 方法"
linktitle: "get_TempFolder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_TempFolder 方法。指定在保存为 DOC 或 DOCX 文件时用于临时文件的文件夹。默认情况下，此属性为 null，C++ 中不使用临时文件。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


指定在保存为 DOC 或 DOCX 文件时使用的临时文件夹。默认情况下，此属性为 **null**，且不使用临时文件。

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## 备注


当 Aspose.Words 保存文档时，需要创建临时的内部结构。默认情况下，这些内部结构会在内存中创建，在文档保存期间内存使用会短暂飙升。保存完成后，内存会被释放并由垃圾回收器回收。

使用 [TempFolder](./) 指定临时文件夹后，Aspose.Words 将把内部结构保存在临时文件中而不是内存中。这可以降低保存过程中的内存使用，但会降低保存性能。

文件夹必须存在且可写，否则将抛出异常。

Aspose.Words 在保存完成后会自动删除所有临时文件。

## 示例



展示在保存文档时如何使用硬盘而不是内存。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 当我们保存文档时，各种元素会在保存操作进行时临时存储在内存中。
// 我们可以使用此选项改为在本地文件系统中使用临时文件夹，
// 这将减少我们应用程序的内存开销。
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// 指定的临时文件夹必须在保存操作之前存在于本地文件系统中。
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// 该文件夹将在加载操作后保持存在且不含残留内容。
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## 另见

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
