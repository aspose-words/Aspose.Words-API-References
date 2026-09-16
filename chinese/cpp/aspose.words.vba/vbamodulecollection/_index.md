---
title: "Aspose::Words::Vba::VbaModuleCollection 类"
linktitle: "VbaModuleCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaModuleCollection 类。表示 VbaModule 对象的集合。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class


表示一组 [VbaModule](../vbamodule/) 对象。要了解更多，请访问 [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) 文档文章。

```cpp
class VbaModuleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Vba::VbaModule>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Vba::VbaModule\>\&) | 向集合中添加模块。 |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | 返回集合中 VBA 模块的数量。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 通过索引检索 [VbaModule](../vbamodule/) 对象。 |
| [idx_get](./idx_get/)(const System::String\&) | 通过名称检索 [VbaModule](../vbamodule/) 对象，如果未找到则返回 Null。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Vba::VbaModule\>\&) | 从集合中移除指定的模块。 |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| 类型定义 | 描述 |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## 示例



展示如何访问文档的 VBA 项目信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// VBA 项目包含一组 VBA 模块。
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// 为 VBA 模块设置新的源代码。您可以通过索引或名称访问集合中的 VBA 模块。
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// 从集合中移除模块。
vbaModules->Remove(vbaModules->idx_get(2));
```

## 另见

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
