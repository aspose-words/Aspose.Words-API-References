---
title: "Aspose::Words::Vba::VbaModuleType 枚举"
linktitle: "VbaModuleType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaModuleType 枚举。指定在 C++ 中 VBA 项目模型的类型。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


指定 VBA 项目中模型的类型。

```cpp
enum class VbaModuleType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| DocumentModule | 0 | VBA 项目项的一种类型，指定用于嵌入宏和与文档关联的编程访问操作的模块。 |
| ProceduralModule | 1 | 子程序和函数的集合。 |
| ClassModule | 2 | 包含新对象定义的模块。类的每个实例都会创建一个新对象，模块中定义的过程会成为对象的属性和方法。 |
| DesignerModule | 3 | 一个 VBA 模块，扩展已在项目中注册的 ActiveX 控件的方法和属性。 |


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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
