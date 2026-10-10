---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Id Methode"
linktitle: "get_Id"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Id Methode. Gibt eine eindeutige schreibgeschützte persistente numerische Id für dieses SDT in C++ an."
type: docs
weight: 17000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_id/
---
## StructuredDocumentTag::get_Id method


Gibt eine eindeutige schreibgeschützte persistente numerische Id für dieses **SDT** an.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_Id() override
```

## Hinweise


Id-Attribut muss folgenden Regeln entsprechen:* Das Dokument behält SDT-Ids nur bei, wenn das gesamte Dokument geklont wird [Clone](../../../aspose.words/document/clone/).
* During [ImportNode()](../) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
* If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone SDT [Clone()](../) operation new unique ID will be generated for the cloned SDT node.
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.



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
