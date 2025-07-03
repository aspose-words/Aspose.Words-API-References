---
title: Aspose::Words::Comment::get_DateTimeUtc method
linktitle: get_DateTimeUtc
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment::get_DateTimeUtc method. Gets the UTC date and time that the comment was made in C++.'
type: docs
weight: 7500
url: /cpp/aspose.words/comment/get_datetimeutc/
---
## Comment::get_DateTimeUtc method


Gets the UTC date and time that the comment was made.

```cpp
System::DateTime Aspose::Words::Comment::get_DateTimeUtc()
```


## Examples



Shows how to get UTC date and time. 
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
// DateTimeUtc return data without milliseconds.
ASSERT_EQ(dateTime.ToUniversalTime().ToString(u"yyyy-MM-dd hh:mm:ss"), comment->get_DateTimeUtc().ToString(u"yyyy-MM-dd hh:mm:ss"));
```

## See Also

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
