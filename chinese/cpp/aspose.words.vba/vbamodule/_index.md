---
title: "Aspose::Words::Vba::VbaModule 类"
linktitle: "VbaModule"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaModule 类。提供对 VBA 项目模块的访问。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


提供对 VBA 项目模块的访问。要了解更多信息，请访问 [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) 文档文章。

```cpp
class VbaModule : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clone](./clone/)() | 执行对 [VbaModule](./) 的复制。 |
| [get_Name](./get_name/)() const | 获取或设置 VBA 项目模块名称。 |
| [get_SourceCode](./get_sourcecode/)() const | 获取或设置 VBA 项目模块源代码。 |
| [get_Type](./get_type/)() const | 指定模块是过程模块、文档模块、类模块还是设计器模块。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | 用于 [Aspose::Words::Vba::VbaModule::get_Name](./get_name/) 的设置器。 |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | 用于 [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/) 的设置器。 |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | 用于 [Aspose::Words::Vba::VbaModule::get_Type](./get_type/) 的设置器。 |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | 创建一个空模块。 |

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
