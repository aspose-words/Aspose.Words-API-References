---
title: "Aspose::Words::Document::get_VbaProject 方法"
linktitle: "get_VbaProject"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_VbaProject 方法。获取或设置 C++ 中的 VbaProject。"
type: docs
weight: 56000
url: /zh/cpp/aspose.words/document/get_vbaproject/
---
## Document::get_VbaProject method


获取或设置一个 [VbaProject](./)。

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Document::get_VbaProject() const
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

* Class [VbaProject](../../../aspose.words.vba/vbaproject/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
