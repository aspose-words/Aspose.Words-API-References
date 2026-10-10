---
title: "Aspose::Words::Layout::LayoutEnumerator 类"
linktitle: "LayoutEnumerator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutEnumerator 类。枚举文档的页面布局实体。您可以使用此类遍历页面布局模型。可用的属性包括类型、几何形状、文本以及实体呈现所在的页面索引，还包括整体结构和关系。使用 GetEntity() 和 Current 的组合可移动到对应文档节点的实体。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


枚举文档的页面布局实体。您可以使用此类遍历页面布局模型。可用属性包括类型、几何形状、文本以及实体呈现所在的页面索引，还包括整体结构和关系。使用 [GetEntity()](../) 和 [Current](./get_current/) 的组合可移动到对应文档节点的实体。欲了解更多，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | 获取或设置页面布局模型中的当前位置信息。此属性返回一个对应当前布局实体的不透明对象。 |
| [get_Document](./get_document/)() const | 获取此实例枚举的文档。 |
| [get_Kind](./get_kind/)() | 获取当前实体的类型。该值可以是空字符串，但永不为 **null**。 |
| [get_PageIndex](./get_pageindex/)() | 获取包含当前实体的页面的 1 基索引。 |
| [get_Rectangle](./get_rectangle/)() | 返回相对于页面左上角（以点为单位）的当前实体的边界矩形。 |
| [get_Text](./get_text/)() | 获取当前跨度实体的文本。对其他实体类型会抛出异常。 |
| [get_Type](./get_type/)() | 获取当前实体的类型。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | 获取实体的命名属性。 |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | 初始化此类的新实例。 |
| [MoveFirstChild](./movefirstchild/)() | 移动到第一个子实体。 |
| [MoveLastChild](./movelastchild/)() | 移动到最后一个子实体。 |
| [MoveNext](./movenext/)() | 按视觉顺序移动到下一个兄弟实体。当遍历跨页段落的行时，此方法不会移动到下一页，而是移动到同一页上的下一个实体。 |
| [MoveNextLogical](./movenextlogical/)() | 按逻辑顺序移动到下一个兄弟实体。当遍历跨页段落的行时，此方法即使在另一页上也会移动到下一行。 |
| [MoveParent](./moveparent/)() | 移动到父实体。 |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | 移动到指定类型的父实体。 |
| [MovePrevious](./moveprevious/)() | 移动到前一个兄弟实体。 |
| [MovePreviousLogical](./movepreviouslogical/)() | 按逻辑顺序移动到前一个兄弟实体。在遍历跨页段落的行时，即使前一行位于另一页，此方法也会移动到前一行。 |
| [Reset](./reset/)() | 将枚举器移动到文档的第一页。 |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | 设置器用于 [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/)。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
