---
title: "Aspose::Words::Drawing::ShapeBase::get_Font metod"
linktitle: "get_Font"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Font metod. Ger åtkomst till teckensnittsformateringen för detta objekt i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words.drawing/shapebase/get_font/
---
## ShapeBase::get_Font method


Tillhandahåller åtkomst till teckensnittsformateringen för detta objekt.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::ShapeBase::get_Font()
```


## Exempel



Visar hur man infogar en textruta och ställer in teckensnittet för dess innehåll.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// Ställ in egenskapen "Hidden" för formens "Font"-objekt till "true" för att dölja textrutan från synen
// och kollapsa det utrymme som den normalt skulle uppta.
// Ställ in egenskapen "Hidden" för formens "Font"-objekt till "false" för att låta textrutan vara synlig.
shape->get_Font()->set_Hidden(hideShape);

// Om formen är synlig kommer vi att ändra dess utseende via teckensnittobjektet.
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// Flytta byggaren från textrutan tillbaka till huvuddokumentet.
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## Se även

* Class [Font](../../../aspose.words/font/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
