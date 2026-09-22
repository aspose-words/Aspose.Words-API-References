---
title: "Aspose::Words::Comment::get_DateTimeUtc yöntemi"
linktitle: "get_DateTimeUtc"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comment::get_DateTimeUtc metodu. Yorumun C++'da yapıldığı UTC tarih ve saatini alır."
type: docs
weight: 7500
url: /tr/cpp/aspose.words/comment/get_datetimeutc/
---
## Comment::get_DateTimeUtc method


Yorumun yapıldığı UTC tarih ve saatini alır.

```cpp
System::DateTime Aspose::Words::Comment::get_DateTimeUtc()
```


## Örnekler



UTC tarih ve saatinin nasıl alınacağını gösterir.
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
// DateTimeUtc, milisaniyesiz veri döndürür.
ASSERT_EQ(dateTime.ToUniversalTime().ToString(u"yyyy-MM-dd hh:mm:ss"), comment->get_DateTimeUtc().ToString(u"yyyy-MM-dd hh:mm:ss"));
```

## Ayrıca Bakınız

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
