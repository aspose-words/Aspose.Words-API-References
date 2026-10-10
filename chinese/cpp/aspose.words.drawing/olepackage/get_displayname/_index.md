---
title: "Aspose::Words::Drawing::OlePackage::get_DisplayName 方法"
linktitle: "get_DisplayName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::OlePackage::get_DisplayName 方法。获取或设置 OLE 包的显示名称（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing/olepackage/get_displayname/
---
## OlePackage::get_DisplayName method


获取或设置 OLE 包显示名称。

```cpp
System::String Aspose::Words::Drawing::OlePackage::get_DisplayName() const
```


## 示例



展示如何将 OLE 对象插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE 对象允许我们使用已安装的其他应用程序打开本地文件系统中的其他文件
// 在我们的操作系统中，通过双击文档正文中包含 OLE 对象的形状来打开。
// 在这种情况下，我们的外部文件将是 ZIP 压缩包。
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## 另见

* Class [OlePackage](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
