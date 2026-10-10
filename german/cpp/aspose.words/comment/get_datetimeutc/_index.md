---
title: "Aspose::Words::Comment::get_DateTimeUtc-Methode"
linktitle: "get_DateTimeUtc"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comment::get_DateTimeUtc-Methode. Ermittelt das UTC-Datum und die UTC-Uhrzeit, zu denen der Kommentar in C++ erstellt wurde."
type: docs
weight: 7500
url: /de/cpp/aspose.words/comment/get_datetimeutc/
---
## Comment::get_DateTimeUtc method


Ermittelt das UTC-Datum und die UTC-Uhrzeit, zu der der Kommentar erstellt wurde.

```cpp
System::DateTime Aspose::Words::Comment::get_DateTimeUtc()
```


## Beispiele



Zeigt, wie man das UTC-Datum und die UTC-Uhrzeit abruft.
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
// DateTimeUtc gibt Daten ohne Millisekunden zurück.
ASSERT_EQ(dateTime.ToUniversalTime().ToString(u"yyyy-MM-dd hh:mm:ss"), comment->get_DateTimeUtc().ToString(u"yyyy-MM-dd hh:mm:ss"));
```

## Siehe auch

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
