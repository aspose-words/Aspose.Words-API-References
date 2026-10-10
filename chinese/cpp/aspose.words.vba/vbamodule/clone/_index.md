---
title: "Aspose::Words::Vba::VbaModule::Clone 方法"
linktitle: "克隆"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaModule::Clone 方法。对 C++ 中的 VbaModule 执行复制操作。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.vba/vbamodule/clone/
---
## VbaModule::Clone method


对 [VbaModule](../) 执行复制操作。

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModule::Clone()
```


### ReturnValue

已克隆的 [VbaModule](../)。

## 示例



展示如何深度克隆 VBA 项目和模块。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// 在目标文档中，我们已经有一个名为 "Module1" 的模块
// 因为我们在克隆项目时也克隆了它。我们需要删除该模块。
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## 另见

* Class [VbaModule](../)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
