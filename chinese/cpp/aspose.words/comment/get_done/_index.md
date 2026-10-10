---
title: "Aspose::Words::Comment::get_Done 方法"
linktitle: "get_Done"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comment::get_Done 方法。获取或设置标记，指示该评论已在 C++ 中标记为完成。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


获取或设置标记，指示评论已标记为完成。

```cpp
bool Aspose::Words::Comment::get_Done() const
```


## 示例



展示如何将评论标记为 "done"。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// 插入评论以指出错误。
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// 评论具有一个 "Done" 标志，默认设置为 "false"。
// 如果评论建议我们在文档中进行更改，
// 我们可以应用更改，然后再设置 "Done" 标志以指示已纠正。
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// 已标记为 "done" 的评论会自行区分
// 与未标记为 "done" 的评论使用淡化的文字颜色区分。
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## 另见

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
