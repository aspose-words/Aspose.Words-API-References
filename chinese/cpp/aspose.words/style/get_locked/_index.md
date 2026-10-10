---
title: "Aspose::Words::Style::get_Locked 方法"
linktitle: "get_Locked"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_Locked 方法。指定此样式在 C++ 中是否被锁定。"
type: docs
weight: 13500
url: /zh/cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


指定此样式是否被锁定。

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## 示例



展示如何锁定样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```

## 另见

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
