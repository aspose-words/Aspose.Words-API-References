---
title: "Aspose::Words::TabStopCollection::Add metod"
linktitle: "Add"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TabStopCollection::Add metod. Lägger till eller ersätter ett tabbstopp i samlingen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


Lägger till eller ersätter ett tabbstopp i samlingen.

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tabbstopp | const System::SharedPtr\<Aspose::Words::TabStop\>\& | Ett tabbstopp-objekt att lägga till. |
## Anmärkningar


Om ett tabbstopp redan finns på den angivna positionen ersätts det.

## Exempel



Visar hur man lägger till anpassade tabbstopp i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Nedan följer två sätt att lägga till tabbstopp i ett stycke via egenskapen "ParagraphFormat".
// 1 -  Skapa ett "TabStop"‑objekt och lägg sedan till det i samlingen:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Skicka värdena för egenskaperna för ett nytt tabbstopp till "Add"-metoden:
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Lägg till tabbstopp på 5 cm i alla stycken.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Varje "tab"-tecken flyttar byggarens markör till platsen för nästa tabbstopp.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Se även

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


Lägger till eller ersätter ett tabbstopp i samlingen.

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| position | double | En position (i punkter) där tabbstoppet ska läggas till. |
| alignment | Aspose::Words::TabAlignment | Ett [TabAlignment](../../tabalignment/)‑värde som specificerar justeringen av texten vid tabbstoppet. |
| leader | Aspose::Words::TabLeader | Ett [TabLeader](../../tableader/)‑värde som specificerar typen av ledarlinje som visas under tab‑tecknet. |
## Anmärkningar


Om ett tabbstopp redan finns på den angivna positionen ersätts det.

## Exempel



Visar hur man lägger till anpassade tabbstopp i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Nedan följer två sätt att lägga till tabbstopp i ett stycke via egenskapen "ParagraphFormat".
// 1 -  Skapa ett "TabStop"‑objekt och lägg sedan till det i samlingen:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Skicka värdena för egenskaperna för ett nytt tabbstopp till "Add"-metoden:
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Lägg till tabbstopp på 5 cm i alla stycken.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Varje "tab"-tecken flyttar byggarens markör till platsen för nästa tabbstopp.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Se även

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
