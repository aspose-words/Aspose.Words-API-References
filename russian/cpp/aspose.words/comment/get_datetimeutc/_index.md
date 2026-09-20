---
title: "Aspose::Words::Comment::get_DateTimeUtc метод"
linktitle: "get_DateTimeUtc"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Comment::get_DateTimeUtc. Получает дату и время в UTC, когда был сделан комментарий, в C++."
type: docs
weight: 7500
url: /ru/cpp/aspose.words/comment/get_datetimeutc/
---
## Comment::get_DateTimeUtc method


Получает дату и время UTC создания комментария.

```cpp
System::DateTime Aspose::Words::Comment::get_DateTimeUtc()
```


## Примеры



Показывает, как получить дату и время в UTC.
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
// DateTimeUtc возвращает данные без миллисекунд.
ASSERT_EQ(dateTime.ToUniversalTime().ToString(u"yyyy-MM-dd hh:mm:ss"), comment->get_DateTimeUtc().ToString(u"yyyy-MM-dd hh:mm:ss"));
```

## См. также

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
