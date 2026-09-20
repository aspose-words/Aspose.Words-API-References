---
title: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet 方法"
linktitle: "get_SavePictureBullet"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet 方法。当为 false 时，PictureBullet 数据不会保存到输出文档。默认值在 C++ 中为 true。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


当 **false** 时，PictureBullet 数据不会保存到输出文档。默认值为 **true**。

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## 备注


此选项针对 Word 97 提供，因为它无法正确处理 PictureBullet 数据。要移除 PictureBullet 数据，请将该选项设为 "false"。

## 示例



展示在保存时如何省略文档中的 PictureBullet 数据。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// 某些文字处理器，例如 Microsoft Word 97，与 PictureBullet 数据不兼容。
// 通过在 SaveOptions 对象中设置标志，
// 我们可以在保存时将所有图像项目符号转换为普通项目符号。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## 另见

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
