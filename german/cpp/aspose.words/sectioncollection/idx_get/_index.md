---
title: "Aspose::Words::SectionCollection::idx_get-Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::SectionCollection::idx_get-Methode. Ruft einen Abschnitt am angegebenen Index in C++ ab."
type: docs
weight: 3000
url: /de/cpp/aspose.words/sectioncollection/idx_get/
---
## SectionCollection::idx_get method


Ruft einen Abschnitt am angegebenen Index ab.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::SectionCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Ein Index in die Liste der Abschnitte. |
## Hinweise


Der Index ist nullbasiert.

Negative Indizes sind erlaubt und bedeuten Zugriff vom Ende der Sammlung. Zum Beispiel bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer als oder gleich der Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

Wenn der Index negativ ist und sein absoluter Wert größer ist als die Anzahl der Elemente in der Liste, gibt dies eine Nullreferenz zurück.

## Beispiele



Zeigt, wann das Seitenlayout des Dokuments neu berechnet werden muss.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Das Speichern eines Dokuments als PDF, als Bild oder das erstmalige Drucken wird automatisch
// Cache das Layout des Dokuments innerhalb seiner Seiten.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Das Dokument auf irgendeine Weise ändern.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// In der aktuellen Version von Aspose.Words wird das Dokument beim Ändern nicht automatisch neu aufgebaut
// das zwischengespeicherte Seitenlayout. Wenn wir möchten, dass das zwischengespeicherte Layout
// auf dem neuesten Stand bleibt, müssen wir es manuell aktualisieren.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```


Zeigt, wie man einen neuen Abschnittsknoten zur Bearbeitung vorbereitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält einen Abschnitt, der einen Body hat, der wiederum einen Paragraphen enthält.
// Wir können diesem Dokument Inhalte hinzufügen, indem wir Elemente wie Textläufe, Formen oder Tabellen zu diesem Paragraphen hinzufügen.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Wenn wir einen neuen Abschnitt auf diese Weise hinzufügen, hat er keinen Body oder andere Kindknoten.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Führen Sie die Methode "EnsureMinimum" aus, um diesem Abschnitt einen Body und einen Paragraphen hinzuzufügen, damit Sie mit der Bearbeitung beginnen können.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Siehe auch

* Class [Section](../../section/)
* Class [SectionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
