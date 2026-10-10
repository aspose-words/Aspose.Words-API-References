---
title: "Aspose::Words::DocumentBuilder::PopFont metod"
linktitle: "PopFont"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::PopFont metod. Hämtar teckenformatering som tidigare sparats på stacken i C++."
type: docs
weight: 62000
url: /sv/cpp/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder::PopFont method


Hämtar teckenformatering som tidigare sparats på stacken.

```cpp
void Aspose::Words::DocumentBuilder::PopFont()
```


## Exempel



Visar hur man använder en dokumentbyggares formateringsstack.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ställ in teckenformatering, skriv sedan texten som kommer före hyperlänken.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Bevara vår aktuella formateringskonfiguration på stacken.
builder->PushFont();

// Ändra byggarens aktuella formatering genom att tillämpa en ny stil.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Återställ teckenformateringen som vi sparade tidigare och ta bort elementet från stacken.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
