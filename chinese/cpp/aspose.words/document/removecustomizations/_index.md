---
title: "Aspose::Words::Document::RemoveCustomizations 方法"
linktitle: "RemoveCustomizations"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::RemoveCustomizations 方法。移除文档中工具栏和键盘命令的自定义设置（C++）。"
type: docs
weight: 67750
url: /zh/cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


从文档中删除工具栏和键盘命令的自定义。

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## 示例



展示如何从文档中移除工具栏和键盘命令的自定义设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// 移除所有自定义文档 UI 设置，包括自定义上下文菜单项。
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
