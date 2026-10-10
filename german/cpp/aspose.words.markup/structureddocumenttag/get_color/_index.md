---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Color Methode"
linktitle: "get_Color"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Color Methode. Ruft die Farbe des strukturierten Dokument-Tags ab oder legt sie fest in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_color/
---
## StructuredDocumentTag::get_Color method


Liest oder setzt die Farbe des strukturierten Dokument-Tags.

```cpp
System::Drawing::Color Aspose::Words::Markup::StructuredDocumentTag::get_Color() override
```


## Beispiele



Zeigt, wie man ein strukturiertes Dokument-Tag in einem einfachen Textfeld erstellt und dessen Aussehen ändert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie ein strukturiertes Dokument-Tag, das Klartext enthält.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Legen Sie den Titel und die Farbe des Rahmens fest, der erscheint, wenn Sie mit der Maus über das strukturierte Dokument-Tag in Microsoft Word fahren.
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// Legen Sie ein Tag für dieses strukturierte Dokument-Tag fest, das erhältlich ist
// als ein XML-Element mit dem Namen "tag", wobei die untenstehende Zeichenkette im Attribut "@val" enthalten ist.
tag->set_Tag(u"MyPlainTextSDT");

// Jedes strukturierte Dokument-Tag hat eine zufällige eindeutige ID.
ASSERT_TRUE(tag->get_Id() > 0);

// Legen Sie die Schriftart für den Text innerhalb des strukturierten Dokument-Tags fest.
tag->get_ContentsFont()->set_Name(u"Arial");

// Legen Sie die Schriftart für den Text am Ende des strukturierten Dokument-Tags fest.
// Jeder Text, den wir im Dokumentkörper eingeben, nachdem wir das Tag mit den Pfeiltasten verlassen haben, verwendet diese Schriftart.
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// Standardmäßig ist dies false und das Drücken von Enter innerhalb eines strukturierten Dokument-Tags bewirkt nichts.
// Wenn es auf true gesetzt ist, kann unser strukturiertes Dokument-Tag mehrere Zeilen enthalten.

// Setzen Sie die Eigenschaft "Multiline" auf "false", um nur den Inhalt zu erlauben
// dieses strukturierten Dokument-Tags auf eine einzelne Zeile zu beschränken.
// Setzen Sie die Eigenschaft "Multiline" auf "true", um dem Tag zu erlauben, mehrere Zeilen Inhalt zu enthalten.
tag->set_Multiline(true);

// Setzen Sie die Eigenschaft "Appearance" auf "SdtAppearance.Tags", um Tags um den Inhalt anzuzeigen.
// Standardmäßig wird das strukturierte Dokument-Tag als BoundingBox angezeigt.
tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

// Fügen Sie eine Kopie unseres strukturierten Dokument-Tags in einen neuen Absatz ein.
auto tagClone = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(System::ExplicitCast<Aspose::Words::Node>(tag)->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// Verwenden Sie die Methode "RemoveSelfOnly", um ein strukturiertes Dokument-Tag zu entfernen, während dessen Inhalt im Dokument erhalten bleibt.
tagClone->RemoveSelfOnly();

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlainText.docx");
```

## Siehe auch

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
