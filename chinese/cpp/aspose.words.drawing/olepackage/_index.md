---
title: "Aspose::Words::Drawing::OlePackage 类"
linktitle: "OlePackage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::OlePackage 类。允许访问 OLE 包属性。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


允许访问 OLE 包属性。要了解更多信息，请访问 [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/) 文档文章。

```cpp
class OlePackage : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | 获取或设置 OLE 包显示名称。 |
| [get_FileName](./get_filename/)() const | 获取或设置 OLE 包文件名。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | 设置 [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/)。 |
| [set_FileName](./set_filename/)(System::String) | 设置 [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/)。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
