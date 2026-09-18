---
title: "Aspose::Words::Style::get_LinkedStyleName Methode"
linktitle: "get_LinkedStyleName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_LinkedStyleName Methode. Gibt den Namen des mit diesem verknüpften Stils zurück bzw. setzt ihn. Gibt einen leeren String zurück, wenn keine Stile verknüpft sind, in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


Gibt den Namen des [Style](../) zurück, das mit diesem verknüpft ist, bzw. setzt ihn. Gibt einen leeren String zurück, wenn keine Stile verknüpft sind.

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## Hinweise


Es ist nur erlaubt, den Absatzstil mit dem Zeichenstil zu verknüpfen und umgekehrt.

Das Festlegen von LinkedStyleName für den aktuellen Stil führt automatisch zum Festlegen von LinkedStyleName für den verknüpften Stil.

Das Zuweisen eines leeren Strings entspricht dem Aufheben der Verknüpfung des zuvor verknüpften Stils.

## Beispiele



Zeigt, wie man Stil-Aliasse verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// Dieses Dokument enthält einen Stil mit dem Namen "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Wenn der Name eines Stils mehrere durch Kommas getrennte Werte enthält, ist jede Angabe ein separater Alias.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// Wir können einen Stil sowohl über seinen Alias als auch über seinen Namen referenzieren.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```


Zeigt, wie Stile untereinander verknüpft werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);

System::SharedPtr<Aspose::Words::Style> styleHeading1Char = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"Heading 1 Char");
styleHeading1Char->get_Font()->set_Name(u"Verdana");
styleHeading1Char->get_Font()->set_Bold(true);
styleHeading1Char->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::Dot);
styleHeading1Char->get_Font()->get_Border()->set_LineWidth(15);

styleHeading1->set_LinkedStyleName(u"Heading 1 Char");

ASSERT_EQ(u"Heading 1 Char", styleHeading1->get_LinkedStyleName());
ASSERT_EQ(u"Heading 1", styleHeading1Char->get_LinkedStyleName());
```

## Siehe auch

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
