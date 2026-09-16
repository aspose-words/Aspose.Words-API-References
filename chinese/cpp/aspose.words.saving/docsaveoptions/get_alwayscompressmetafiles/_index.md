---
title: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles 方法"
linktitle: "get_AlwaysCompressMetafiles"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles 方法。为 false 时，为了性能原因，小的元文件不会被压缩。默认值为 true，所有元文件都会被压缩，无论其大小，在 C++ 中。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


当 **false** 时，为了性能原因，小的元文件不会被压缩。默认值为 **true**，所有元文件都会被压缩，无论其大小。

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## 示例



展示如何在保存文档时更改元文件的压缩。
```cpp
// 打开包含 Microsoft Equation 3.0 公式的文档。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// 当我们保存文档时，为了性能原因，较小的元文件不会被压缩。
// 我们可以在 SaveOptions 对象中设置标志，以在保存时压缩每个元文件。
// 某些编辑器（如 LibreOffice）无法读取未压缩的元文件。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## 另见

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
