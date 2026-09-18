---
title: "Aspose::Words::TabStopCollection::Add-Methode"
linktitle: "Add"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStopCollection::Add-Methode. Fügt einen Tabstopp zur Sammlung hinzu oder ersetzt ihn in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


Fügt einen Tabulator zur Sammlung hinzu oder ersetzt ihn.

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Tabstopp | const System::SharedPtr\<Aspose::Words::TabStop\>\& | Ein Tabstopp-Objekt zum Hinzufügen. |
## Hinweise


Wenn an der angegebenen Position bereits ein Tabstopp existiert, wird er ersetzt.

## Beispiele



Zeigt, wie benutzerdefinierte Tabstopps zu einem Dokument hinzugefügt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Unten sind zwei Möglichkeiten aufgeführt, Tabstopps über die Eigenschaft "ParagraphFormat" zur Tabstopp‑Sammlung eines Absatzes hinzuzufügen.
// 1 -  Erstelle ein "TabStop"-Objekt und füge es anschließend zur Sammlung hinzu:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Übergib die Werte für die Eigenschaften eines neuen Tabstopps an die Methode "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Füge Tabstopps bei 5 cm zu allen Absätzen hinzu.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Jedes "Tab"‑Zeichen bewegt den Cursor des Builders zur Position des nächsten Tabulators.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Siehe auch

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


Fügt einen Tabulator zur Sammlung hinzu oder ersetzt ihn.

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Position | double | Eine Position (in Punkten), an der der Tabstopp hinzugefügt werden soll. |
| alignment | Aspose::Words::TabAlignment | Ein [TabAlignment](../../tabalignment/)-Wert, der die Ausrichtung des Textes am Tabstopp angibt. |
| leader | Aspose::Words::TabLeader | Ein [TabLeader](../../tableader/)-Wert, der den Typ der Führungslinie angibt, die unter dem Tabulatorzeichen angezeigt wird. |
## Hinweise


Wenn an der angegebenen Position bereits ein Tabstopp existiert, wird er ersetzt.

## Beispiele



Zeigt, wie benutzerdefinierte Tabstopps zu einem Dokument hinzugefügt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Unten sind zwei Möglichkeiten aufgeführt, Tabstopps über die Eigenschaft "ParagraphFormat" zur Tabstopp‑Sammlung eines Absatzes hinzuzufügen.
// 1 -  Erstelle ein "TabStop"-Objekt und füge es anschließend zur Sammlung hinzu:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Übergib die Werte für die Eigenschaften eines neuen Tabstopps an die Methode "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Füge Tabstopps bei 5 cm zu allen Absätzen hinzu.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Jedes "Tab"‑Zeichen bewegt den Cursor des Builders zur Position des nächsten Tabulators.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Siehe auch

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
