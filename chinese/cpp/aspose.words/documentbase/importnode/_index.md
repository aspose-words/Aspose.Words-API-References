---
title: "Aspose::Words::DocumentBase::ImportNode method"
linktitle: "ImportNode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBase::ImportNode 方法。将节点从另一个文档导入到当前文档（C++）。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


将另一个文档的节点导入到当前文档。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | 正在导入的节点。 |
| isImportChildren | bool | **true** 表示递归导入所有子节点；否则为 **false**。 |

### ReturnValue

属于当前文档的克隆节点。
## 备注


此方法使用 [UseDestinationStyles](../../importformatmode/) 选项来解析格式。

导入节点会创建一个属于导入文档的源节点的副本。返回的节点没有父节点。源节点不会被修改或从原始文档中移除。

在将另一个文档的节点插入此文档之前，必须先导入它。导入期间，文档特定的属性（如样式和列表的引用）会从原始文档转换到导入文档。节点导入后，可使用 [InsertBefore1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../) 将其插入文档的适当位置。

如果源节点已经属于目标文档，则仅创建该源节点的深度克隆。

## 示例



展示如何将节点从一个文档导入到另一个文档。
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(dstDoc, u"Destination document first paragraph text."));

// 每个节点都有一个父文档，即包含该节点的文档。
// 将节点插入其不所属的文档会抛出异常。
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(static_cast<std::function<void()>>([&dstDoc, &srcDoc]() -> void
{
    dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(srcDoc->get_FirstSection());
})(), System::ArgumentException);

// 使用 ImportNode 方法创建节点的副本，该副本将拥有文档
// 调用 ImportNode 方法的文档将被设置为其新的拥有文档。
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// 我们现在可以将节点插入文档。
dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(Aspose::Words::SaveFormat::Text));
```

## 另见

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


将节点从另一个文档导入到当前文档，并提供控制格式的选项。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | 要导入的节点。 |
| isImportChildren | bool | **true** 表示递归导入所有子节点；否则为 **false**。 |
| importFormatMode | Aspose::Words::ImportFormatMode | 指定如何合并冲突的样式格式。 |

### ReturnValue

已克隆并导入的节点。该节点属于目标文档，但没有父节点。
## 备注


此重载用于控制样式和列表格式的导入方式，非常有用。

导入节点会创建一个属于导入文档的源节点的副本。返回的节点没有父节点。源节点不会被修改或从原始文档中移除。

在将另一个文档的节点插入此文档之前，必须先导入它。导入期间，文档特定的属性（如样式和列表的引用）会从原始文档转换到导入文档。节点导入后，可使用 [InsertBefore1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../) 将其插入文档的适当位置。

如果源节点已经属于目标文档，则仅创建该源节点的深度克隆。

## 示例



展示如何使用特定选项将节点从源文档导入到目标文档。
```cpp
// 创建两个文档，并向每个文档添加字符样式。
// 配置样式使其具有相同的名称，但文本格式不同。
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
srcStyle->get_Font()->set_Name(u"Courier New");
auto srcBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
srcBuilder->get_Font()->set_Style(srcStyle);
srcBuilder->Writeln(u"Source document text.");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> dstStyle = dstDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
dstStyle->get_Font()->set_Name(u"Calibri");
auto dstBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
dstBuilder->get_Font()->set_Style(dstStyle);
dstBuilder->Writeln(u"Destination document text.");

// 将目标文档中的节导入到源文档，导致样式名称冲突。
// 如果使用目标样式，则具有相同样式名称的导入源文本
// 将作为目标文本采用目标样式。
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// 如果使用 ImportFormatMode.KeepDifferentStyles，则源样式将被保留，
// 并通过添加后缀来解决命名冲突。
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## 另见

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


将节点从另一个文档导入到当前文档，并提供控制格式的选项。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | 要导入的节点。 |
| isImportChildren | bool | **true** 表示递归导入所有子节点；否则为 **false**。 |
| importFormatMode | Aspose::Words::ImportFormatMode | 指定如何合并冲突的样式格式。 |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | 允许指定各种额外的格式化选项。 |

### ReturnValue

已克隆并导入的节点。该节点属于目标文档，但没有父节点。
## 备注


此重载用于控制样式和列表格式的导入方式，非常有用。

导入节点会创建一个属于导入文档的源节点的副本。返回的节点没有父节点。源节点不会被修改或从原始文档中移除。

在将另一个文档的节点插入此文档之前，必须先导入它。导入期间，文档特定的属性（如样式和列表的引用）会从原始文档转换到导入文档。节点导入后，可使用 [InsertBefore1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../) 将其插入文档的适当位置。

如果源节点已经属于目标文档，则仅创建该源节点的深度克隆。

## 示例



展示如何在导入节点时解析形状的源主题颜色。
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// 移动到主页脚并插入使用主题颜色的形状。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// 将源页脚导入到目标文档，并解析主题颜色，
// 因此形状保留来自源文档的实际颜色。
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## 另见

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
