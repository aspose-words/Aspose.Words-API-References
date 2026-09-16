---
title: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName 方法"
linktitle: "get_SuggestedFileName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName 方法。获取当前嵌入对象的建议文件名，如果您想在 C++ 中将其保存到文件中。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


获取当前嵌入对象的建议文件名（如果您想将其保存为文件）。

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## 示例



展示如何获取 OLE 对象的建议文件名。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// OLE 对象可以提供建议的文件名和扩展名，
// 我们可以在将对象内容保存到本地文件系统的文件时使用它们。
System::String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## 另见

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
