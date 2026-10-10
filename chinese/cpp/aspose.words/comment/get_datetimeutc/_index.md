---
title: "Aspose::Words::Comment::get_DateTimeUtc 方法"
linktitle: "get_DateTimeUtc"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comment::get_DateTimeUtc 方法。获取在 C++ 中创建评论的 UTC 日期和时间。"
type: docs
weight: 7500
url: /zh/cpp/aspose.words/comment/get_datetimeutc/
---
## Comment::get_DateTimeUtc method


获取评论创建的 UTC 日期和时间。

```cpp
System::DateTime Aspose::Words::Comment::get_DateTimeUtc()
```


## 示例



展示如何获取 UTC 日期和时间。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::DateTime dateTime = System::DateTime::get_Now();
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", dateTime);
comment->SetText(u"My comment.");

builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.UtcDateTime.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Comment.UtcDateTime.docx");

comment = System::ExplicitCast<Aspose::Words::Comment>(doc->GetChild(Aspose::Words::NodeType::Comment, 0, true));
// DateTimeUtc 返回的数据不包含毫秒。
ASSERT_EQ(dateTime.ToUniversalTime().ToString(u"yyyy-MM-dd hh:mm:ss"), comment->get_DateTimeUtc().ToString(u"yyyy-MM-dd hh:mm:ss"));
```

## 另见

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
