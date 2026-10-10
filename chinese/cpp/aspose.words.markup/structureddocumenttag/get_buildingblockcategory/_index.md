---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory 方法"
linktitle: "get_BuildingBlockCategory"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory 方法。指定此 SDT 节点的构建块类别。在 C++ 中不能为空。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockcategory/
---
## StructuredDocumentTag::get_BuildingBlockCategory method


指定此 **SDT** 节点的构建块类别。不能为空 **null**。

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory()
```

## 备注


访问此属性仅适用于 [BuildingBlockGallery](../../sdttype/) 和 [DocPartObj](../../sdttype/) SDT 类型。对于文档部件类型的 **SDT**，它是只读的。

对于所有其他 SDT 类型，将会出现异常。

## 示例



展示如何将结构化文档标签插入为构建块，并设置其类别和库。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::BuildingBlockGallery, Aspose::Words::Markup::MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## 另见

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
