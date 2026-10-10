---
title: "Aspose::Words::ParagraphCollection::ToArray 方法"
linktitle: "ToArray"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphCollection::ToArray 方法。将集合中的所有段落复制到 C++ 中的新段落数组。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


将集合中的所有段落复制到一个新的段落数组中。

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

段落数组。

## 示例



展示如何从 [NodeCollection](../../nodecollection/) 创建数组。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


展示如何使用 “hot remove” 在枚举期间删除节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// 在枚举过程中从集合中删除节点。
for (System::SharedPtr<Aspose::Words::Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## 另见

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
