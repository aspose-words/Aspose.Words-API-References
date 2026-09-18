---
title: "Aspose::Words::DocumentBuilder::InsertParagraph method"
linktitle: "InsertParagraph"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertParagraph-Methode. Fügt einen Absatzumbruch in das Dokument in C++ ein."
type: docs
weight: 44000
url: /de/cpp/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder::InsertParagraph method


Fügt einen Absatzumbruch in das Dokument ein.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::InsertParagraph()
```


### ReturnValue

Der Absatzknoten, der gerade eingefügt wurde. Es ist derselbe Knoten wie [CurrentParagraph](../get_currentparagraph/).
## Hinweise


Die aktuelle Absatzformatierung, die durch die Eigenschaft [ParagraphFormat](../get_paragraphformat/) angegeben ist, wird verwendet.

Teilt den aktuellen Absatz in zwei. Nach dem Einfügen des Absatzes wird der Cursor an den Anfang des neuen Absatzes gesetzt.

Eine Ausnahme wird ausgelöst, wenn es nicht möglich ist, an der aktuellen Cursorposition einen Absatzumbruch einzufügen.

## Beispiele



Zeigt, wie man einen Absatz in das Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// Die Methode "Writeln" beendet den Absatz nach dem Anhängen von Text
// und startet dann eine neue Zeile, wodurch ein neuer Absatz hinzugefügt wird.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## Siehe auch

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
