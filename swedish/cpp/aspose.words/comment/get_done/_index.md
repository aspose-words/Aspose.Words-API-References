---
title: "Aspose::Words::Comment::get_Done metod"
linktitle: "get_Done"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comment::get_Done metod. Hämtar eller anger flagga som indikerar att kommentaren har markerats som klar i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


Hämtar eller anger flagga som indikerar att kommentaren har markerats som klar.

```cpp
bool Aspose::Words::Comment::get_Done() const
```


## Exempel



Visar hur man markerar en kommentar som "klar".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Infoga en kommentar för att påpeka ett fel.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Kommentarer har en "Klar"-flagga som som standard är satt till "false".
// Om en kommentar föreslår att vi gör en ändring i dokumentet,
// vi kan tillämpa ändringen och sedan också sätta "Done"-flaggan efteråt för att indikera korrigeringen.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Kommentarer som är "done" kommer att skilja sig
// från de som inte är "done" med en blekt textfärg.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Se även

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
