---
title: "Aspose::Words::Vba::VbaModuleCollection::idx_get method"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaModuleCollection::idx_get 方法。在 C++ 中按名称检索 VbaModule 对象，如果未找到则返回 Null。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.vba/vbamodulecollection/idx_get/
---
## VbaModuleCollection::idx_get(const System::String\&) method


按名称检索一个 [VbaModule](../../vbamodule/) 对象，如果未找到则返回 Null。

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModuleCollection::idx_get(const System::String &name)
```


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

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
## VbaModuleCollection::idx_get(int32_t) method


按索引检索一个 [VbaModule](../../vbamodule/) 对象。

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModuleCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 要检索的模块的零基索引。 |

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

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
