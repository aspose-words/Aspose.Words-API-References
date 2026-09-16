---
title: "Aspose::Words::Vba::VbaProject::VbaProject 构造函数"
linktitle: "VbaProject"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaProject::VbaProject 构造函数。创建一个空白的 VbaProject（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject::VbaProject constructor


创建一个空白的 [VbaProject](../)。

```cpp
Aspose::Words::Vba::VbaProject::VbaProject()
```


## 示例



展示如何使用宏创建 VBA 项目。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建新的 VBA 项目。
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// 创建新模块并指定宏源代码。
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// 将模块添加到 VBA 项目中。
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## 另见

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
