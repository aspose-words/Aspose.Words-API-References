---
title: "Aspose::Words::Comment::get_DateTimeUtc metodo"
linktitle: "get_DateTimeUtc"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Comment::get_DateTimeUtc. Ottiene la data e l'ora UTC in cui è stato creato il commento in C++."
type: docs
weight: 7500
url: /it/cpp/aspose.words/comment/get_datetimeutc/
---
## Comment::get_DateTimeUtc method


Ottiene la data e l'ora UTC in cui è stato effettuato il commento.

```cpp
System::DateTime Aspose::Words::Comment::get_DateTimeUtc()
```


## Esempi



Mostra come ottenere la data e l'ora UTC.
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
// DateTimeUtc restituisce i dati senza millisecondi.
ASSERT_EQ(dateTime.ToUniversalTime().ToString(u"yyyy-MM-dd hh:mm:ss"), comment->get_DateTimeUtc().ToString(u"yyyy-MM-dd hh:mm:ss"));
```

## Vedi anche

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
