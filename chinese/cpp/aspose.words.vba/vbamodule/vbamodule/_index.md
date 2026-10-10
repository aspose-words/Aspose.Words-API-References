---
title: "Aspose::Words::Vba::VbaModule::VbaModule 构造函数"
linktitle: "VbaModule"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaModule::VbaModule 构造函数。创建一个 C++ 中的空模块。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule::VbaModule constructor


创建一个空模块。

```cpp
Aspose::Words::Vba::VbaModule::VbaModule()
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

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
