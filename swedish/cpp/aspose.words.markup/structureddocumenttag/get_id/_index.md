---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Id metod"
linktitle: "get_Id"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Id metod. Anger ett unikt skrivskyddat beständigt numeriskt Id för detta SDT i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.markup/structureddocumenttag/get_id/
---
## StructuredDocumentTag::get_Id method


Anger ett unikt skrivskyddat bestående numeriskt Id för denna **SDT**.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_Id() override
```

## Anmärkningar


Id-attributet ska följa dessa regler:* Dokumentet ska behålla SDT-id:n endast om hela dokumentet klonas [Clone](../../../aspose.words/document/clone/).
* During [ImportNode()](../) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
* If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone SDT [Clone()](../) operation new unique ID will be generated for the cloned SDT node.
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.



## Exempel



Visar hur man skapar en strukturerad dokumenttagg i en vanlig textruta och ändrar dess utseende.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa en strukturerad dokumenttagg som kommer att innehålla vanlig text.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Ställ in titel och färg på ramen som visas när du för musen över den strukturerade dokumenttaggen i Microsoft Word.
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// Ange en tagg för denna strukturerade dokumenttagg, som är tillgänglig
// som ett XML‑element med namnet "tag", med strängen nedan i dess "@val"‑attribut.
tag->set_Tag(u"MyPlainTextSDT");

// Varje strukturerad dokumenttagg har ett slumpmässigt unikt ID.
ASSERT_TRUE(tag->get_Id() > 0);

// Ställ in teckensnittet för texten inne i den strukturerade dokumenttaggen.
tag->get_ContentsFont()->set_Name(u"Arial");

// Ställ in teckensnittet för texten i slutet av den strukturerade dokumenttaggen.
// All text som vi skriver i dokumentkroppen efter att ha flyttat ut ur taggen med piltangenter kommer att använda detta teckensnitt.
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// Som standard är detta falskt och att trycka på Enter medan du är inne i en strukturerad dokumenttagg gör ingenting.
// När den är inställd på true kan vår strukturerade dokumenttagg ha flera rader.

// Ställ in egenskapen "Multiline" till "false" för att endast tillåta innehållet
// för denna strukturerade dokumenttagg att sträcka sig över en enda rad.
// Ställ in egenskapen "Multiline" till "true" för att tillåta taggen att innehålla flera rader med innehåll.
tag->set_Multiline(true);

// Ställ in egenskapen "Appearance" till "SdtAppearance.Tags" för att visa taggar runt innehållet.
// Som standard visas strukturerad dokumenttagg som BoundingBox.
tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

// Infoga en klon av vår strukturerade dokumenttagg i ett nytt stycke.
auto tagClone = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(System::ExplicitCast<Aspose::Words::Node>(tag)->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// Använd metoden "RemoveSelfOnly" för att ta bort en strukturerad dokumenttagg, samtidigt som dess innehåll behålls i dokumentet.
tagClone->RemoveSelfOnly();

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlainText.docx");
```

## Se även

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
