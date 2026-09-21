---
title: "Aspose::Words::Comment::Comment‑konstruktor"
linktitle: "Kommentar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comment::Comment‑konstruktor. Initierar en ny instans av Comment‑klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Initierar en ny instans av klassen [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
## Anmärkningar


När [Comment](../) skapas tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och [ParentNode](../../node/get_parentnode/) är **null**.

För att lägga till [Comment](../) i dokumentet, använd [InsertAfter1()</see> eller <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) på det stycke där du vill att kommentaren infogas.

Efter att ha skapat en kommentar, glöm inte att sätta dess [Author](../get_author/), [Initial](../get_initial/) och [DateTime](../get_datetime/) egenskaper.

## Se även

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


Initierar en ny instans av klassen [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
| författare | const System::String\& | Författarnamnet för kommentaren. Får inte vara **null**. |
| initial | const System::String\& | Författarens initialer för kommentaren. Får inte vara **null**. |
| dateTime | System::DateTime | Datum och tid för kommentaren. |

## Exempel



Visar hur man lägger till en kommentar i ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// I Microsoft Word kan vi högerklicka på den här kommentaren i dokumentkroppen för att redigera den, eller svara på den.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Se även

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
