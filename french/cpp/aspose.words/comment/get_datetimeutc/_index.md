---
title: "Aspose::Words::Comment::get_DateTimeUtc méthode"
linktitle: "get_DateTimeUtc"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comment::get_DateTimeUtc méthode. Obtient la date et l'heure UTC auxquelles le commentaire a été créé en C++."
type: docs
weight: 7500
url: /fr/cpp/aspose.words/comment/get_datetimeutc/
---
## Comment::get_DateTimeUtc method


Obtient la date et l'heure UTC auxquelles le commentaire a été fait.

```cpp
System::DateTime Aspose::Words::Comment::get_DateTimeUtc()
```


## Exemples



Montre comment obtenir la date et l'heure UTC.
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
// DateTimeUtc renvoie les données sans millisecondes.
ASSERT_EQ(dateTime.ToUniversalTime().ToString(u"yyyy-MM-dd hh:mm:ss"), comment->get_DateTimeUtc().ToString(u"yyyy-MM-dd hh:mm:ss"));
```

## Voir aussi

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
