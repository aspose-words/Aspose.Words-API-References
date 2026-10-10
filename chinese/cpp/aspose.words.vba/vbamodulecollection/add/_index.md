---
title: "Aspose::Words::Vba::VbaModuleCollection::Add method"
linktitle: "Add"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaModuleCollection::Add 方法。在 C++ 中向集合添加一个模块。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection::Add method


向集合中添加模块。

```cpp
void Aspose::Words::Vba::VbaModuleCollection::Add(const System::SharedPtr<Aspose::Words::Vba::VbaModule> &vbaModule)
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

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
