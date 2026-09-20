---
title: "Aspose::Words::Vba::VbaProject 类"
linktitle: "VbaProject"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaProject 类。提供对 VBA 项目信息的访问。文档中的 VBA 项目被定义为 VBA 模块的集合。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


提供对 VBA 项目信息的访问。文档中的 VBA 项目被定义为 VBA 模块的集合。要了解更多信息，请访问 [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) 文档文章。

```cpp
class VbaProject : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clone](./clone/)() | 执行对 [VbaProject](./) 的复制。 |
| [get_CodePage](./get_codepage/)() const | 获取或设置 VBA 项目的代码页。 |
| [get_IsProtected](./get_isprotected/)() | 显示 [VbaProject](./) 是否受密码保护。 |
| [get_IsSigned](./get_issigned/)() | 显示 [VbaProject](./) 是否已签名。 |
| [get_Modules](./get_modules/)() | 返回 VBA 项目模块的集合。 |
| [get_Name](./get_name/)() const | 获取或设置 VBA 项目名称。 |
| [get_References](./get_references/)() | 获取 VBA 项目引用的集合。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/) 的设置器。 |
| [set_Name](./set_name/)(const System::String\&) | [Aspose::Words::Vba::VbaProject::get_Name](./get_name/) 的设置器。 |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | 创建一个空白的 [VbaProject](./)。 |

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
