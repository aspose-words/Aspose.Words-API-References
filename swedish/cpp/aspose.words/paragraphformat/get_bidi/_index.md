---
title: "Aspose::Words::ParagraphFormat::get_Bidi method"
linktitle: "get_Bidi"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_Bidi method. Hämtar eller anger huruvida detta är ett höger‑till‑vänster stycke i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


Hämtar eller anger om detta är ett stycke med höger-till-vänster-riktning.

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## Anmärkningar


När **true**, körningarna och andra inline-objekt i detta stycke läggs ut från höger till vänster.

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


Visar hur man upptäcker textens riktning i ett klartextdokument.
```cpp
// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett klartextdokument.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Ställ in egenskapen "DocumentDirection" till "DocumentDirection.Auto" för att automatiskt upptäcka
// riktningen för varje textparagraf som Aspose.Words laddar från klartext.
// Varje stycke's "Bidi"-egenskap lagrar dess riktning.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Detektera hebreisk text som från höger till vänster.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Detektera engelsk text som från höger till vänster.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
