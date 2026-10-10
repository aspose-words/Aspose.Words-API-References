---
title: "Aspose::Words::Lists::ListLevel::RemoveTabStop 方法"
linktitle: "RemoveTabStop"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListLevel::RemoveTabStop 方法。移除 C++ 中列表级别的制表位。"
type: docs
weight: 22500
url: /zh/cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


从列表级别中移除制表位。

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## 示例



展示如何清除列表级别的制表位。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建具有默认格式的列表
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// 获取列表级别并移除其制表位
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## 另见

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
