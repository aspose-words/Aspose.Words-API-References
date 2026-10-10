---
title: "Aspose::Words::CommentCollection class"
linktitle: "CommentCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CommentCollection class. Tillhandahåller typad åtkomst till en samling av Comment‑noder. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/commentcollection/
---
## CommentCollection class


Tillhandahåller typad åtkomst till en samling av [Comment](../comment/) noder. För att lära dig mer, besök dokumentationsartikeln [Arbeta med kommentarer](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class CommentCollection : public Aspose::Words::NodeCollection
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Lägger till en nod i slutet av samlingen. |
| [Clear](../nodecollection/clear/)() | Tar bort alla noder från denna samling och från dokumentet. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Avgör om en nod finns i samlingen. |
| [get_Count](../nodecollection/get_count/)() | Hämtar antalet noder i samlingen. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Tillhandahåller en enkel "foreach"‑liknande iteration över samlingen av noder. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar en [Comment](../comment/) på det angivna indexet. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Infogar en nod i samlingen på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Tar bort noden på det angivna indexet från samlingen och från dokumentet. |
| [ToArray](../nodecollection/toarray/)() | Kopierar alla noder från samlingen till en ny nodarray. |
| static [Type](./type/)() |  |

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

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
