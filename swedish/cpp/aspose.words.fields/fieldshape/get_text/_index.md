---
title: "Aspose::Words::Fields::FieldShape::get_Text‑metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldShape::get_Text‑metod. Hämtar eller anger texten att återfå i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldshape/get_text/
---
## FieldShape::get_Text method


Hämtar eller anger texten som ska hämtas.

```cpp
System::String Aspose::Words::Fields::FieldShape::get_Text()
```


## Exempel



Visar hur man skapar listor som är kompatibla med språk som skrivs från höger till vänster med BIDIOUTLINE-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// BIDIOUTLINE-fältet numrerar stycken som AUTONUM/LISTNUM-fälten,
// men är endast synligt när ett språk för redigering från höger till vänster är aktiverat, till exempel hebreiska eller arabiska.
// Följande fält kommer att visa ".1", den RTL‑ekvivalenten till listnumret "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// Lägg till två ytterligare BIDIOUTLINE-fält, som kommer att visa ".2" och ".3".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Ställ in horisontell textjustering för varje stycke i dokumentet till RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Om vi aktiverar ett höger-till-vänster redigeringsspråk i Microsoft Word kommer våra fält att visa siffror.
// Annars kommer de att visa "###".
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


Visar hur vissa äldre Microsoft Word-fält som SHAPE och EMBED hanteras vid inläsning.
```cpp
// Öppna ett dokument som skapades i Microsoft Word 2003.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy fields.doc");

// Om vi öppnar Word-dokumentet och trycker på Alt+F9 kommer vi att se ett SHAPE- och ett EMBED-fält.
// Ett SHAPE-fält är ankaret/duken för ett AutoShape-objekt med omslagstilen "I linje med text" aktiverad.
// Ett EMBED-fält har samma funktion, men för ett inbäddat objekt,
// såsom ett kalkylblad från ett externt Excel-dokument.
// Dessa fält kommer dock inte att visas i dokumentets Fields-samling.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// Dessa fält stöds endast av gamla versioner av Microsoft Word.
// Dokumentets inläsningsprocess kommer att konvertera dessa fält till Shape-objekt,
// som vi kan komma åt i dokumentets nodsamling.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// Den första Shape-noden motsvarar SHAPE-fältet i inmatningsdokumentet,
// vilket är den inlinje-duken för AutoShape.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Image, shape->get_ShapeType());

// Den andra Shape-noden är själva AutoShape.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Can, shape->get_ShapeType());

// Den tredje Shape är det som var EMBED-fältet som innehöll det externa kalkylbladet.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(2));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::OleObject, shape->get_ShapeType());
```

## Se även

* Class [FieldShape](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
