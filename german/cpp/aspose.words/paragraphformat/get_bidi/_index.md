---
title: "Aspose::Words::ParagraphFormat::get_Bidi-Methode"
linktitle: "get_Bidi"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_Bidi-Methode. Gibt an oder legt fest, ob dies ein Rechts-nach-Links-Absatz in C++ ist."
type: docs
weight: 6000
url: /de/cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


Liest oder legt fest, ob dies ein rechts‑nach‑links‑Absatz ist.

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## Hinweise


Wenn **true**, werden die Läufe und anderen Inline-Objekte in diesem Absatz von rechts nach links angeordnet.

## Beispiele



Zeigt, wie man rechts-nach-links-kompatible Listen mit BIDIOUTLINE-Feldern erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Das BIDIOUTLINE-Feld nummeriert Absätze wie die AUTONUM/LISTNUM-Felder,
// ist jedoch nur sichtbar, wenn eine rechts-nach-links Bearbeitungssprache aktiviert ist, wie Hebräisch oder Arabisch.
// Das folgende Feld zeigt ".1" an, das RTL-Äquivalent der Listennummer "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// Fügen Sie zwei weitere BIDIOUTLINE-Felder hinzu, die ".2" und ".3" anzeigen.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Setzen Sie die horizontale Textausrichtung für jeden Absatz im Dokument auf RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Wenn wir in Microsoft Word eine rechts-nach-links Bearbeitungssprache aktivieren, zeigen unsere Felder Zahlen an.
// Andernfalls zeigen sie "###" an.
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


Zeigt, wie man die Textflussrichtung eines Klartextdokuments erkennt.
```cpp
// Erstelle ein \"TxtLoadOptions\"‑Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Setze die Eigenschaft \"DocumentDirection\" auf \"DocumentDirection.Auto\", erkennt automatisch
// die Richtung jedes Textabsatzes, den Aspose.Words aus Klartext lädt.
// Die \"Bidi\"‑Eigenschaft jedes Absatzes speichert dessen Richtung.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Hebräischen Text als rechts‑nach‑links erkennen.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Englischen Text als rechts‑nach‑links erkennen.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
