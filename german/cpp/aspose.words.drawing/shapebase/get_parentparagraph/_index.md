---
title: "Aspose::Words::Drawing::ShapeBase::get_ParentParagraph Methode"
linktitle: "get_ParentParagraph"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_ParentParagraph Methode. Gibt den unmittelbaren übergeordneten Absatz in C++ zurück."
type: docs
weight: 41000
url: /de/cpp/aspose.words.drawing/shapebase/get_parentparagraph/
---
## ShapeBase::get_ParentParagraph method


Gibt den unmittelbaren übergeordneten Absatz zurück.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::ShapeBase::get_ParentParagraph()
```


## Beispiele



Zeigt, wie man ein Textfeld einfügt und die Schriftart seines Inhalts festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// Setzen Sie die "Hidden"-Eigenschaft des "Font"-Objekts der Form auf "true", um das Textfeld vor dem Blick zu verbergen
// und reduzieren Sie den Platz, den es normalerweise einnehmen würde.
// Setzen Sie die "Hidden"-Eigenschaft des "Font"-Objekts der Form auf "false", um das Textfeld sichtbar zu lassen.
shape->get_Font()->set_Hidden(hideShape);

// Wenn die Form sichtbar ist, werden wir ihr Aussehen über das Schriftobjekt ändern.
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// Bewegen Sie den Builder aus dem Textfeld zurück in das Hauptdokument.
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## Siehe auch

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
