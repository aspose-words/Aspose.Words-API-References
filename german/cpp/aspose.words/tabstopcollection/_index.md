---
title: "Aspose::Words::TabStopCollection Klasse"
linktitle: "TabStopCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStopCollection Klasse. Eine Sammlung von TabStop-Objekten, die benutzerdefinierte Tabulatoren für einen Absatz oder einen Stil darstellen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 69000
url: /de/cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


Eine Sammlung von [TabStop](../tabstop/) Objekten, die benutzerdefinierte Tabulatoren für einen Absatz oder einen Stil darstellen. Weitere Informationen finden Sie im Dokumentationsartikel zum [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Fügt einen Tabulator zur Sammlung hinzu oder ersetzt ihn. |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Fügt einen Tabulator zur Sammlung hinzu oder ersetzt ihn. |
| [After](./after/)(double) | Gibt den ersten Tabulator rechts von der angegebenen Position zurück. |
| [Before](./before/)(double) | Gibt den ersten Tabulator links von der angegebenen Position zurück. |
| [Clear](./clear/)() | Löscht alle Tabulatorpositionen. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | Bestimmt, ob die angegebene [TabStopCollection](./) im Wert mit der aktuellen [TabStopCollection](./) gleich ist. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [get_Count](./get_count/)() | Gibt die Anzahl der Tabulatoren in der Sammlung zurück. |
| [GetHashCode](./gethashcode/)() const override | Dient als Hash-Funktion für diesen Typ. |
| [GetIndexByPosition](./getindexbyposition/)(double) | Gibt den Index eines Tabulators mit der angegebenen Position in Punkten zurück. |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | Gibt die Position (in Punkten) des Tabulators am angegebenen Index zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt einen Tabulator am angegebenen Index zurück. |
| [idx_get](./idx_get/)(double) | Gibt einen Tabulator an der angegebenen Position zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveByIndex](./removebyindex/)(int32_t) | Entfernt einen Tabulator am angegebenen Index aus der Sammlung. |
| [RemoveByPosition](./removebyposition/)(double) | Entfernt einen Tabulator an der angegebenen Position aus der Sammlung. |
| static [Type](./type/)() |  |
## Hinweise


In Microsoft Word-Dokumenten kann ein Tabulator in den Eigenschaften eines Absatzstils oder direkt in den Eigenschaften eines Absatzes definiert werden. Ein Stil kann auf einem anderen Stil basieren. Daher ist die vollständige Menge von Tabulatoren für ein gegebenes Objekt eine Kombination aus Tabulatoren, die direkt für dieses Objekt definiert sind, und Tabulatoren, die von den übergeordneten Stilen geerbt werden.

In Aspose.Words enthält eine [TabStopCollection](./), die Sie für einen Absatz oder einen Stil erhalten, nur die benutzerdefinierten Tabulatoren, die direkt für diesen Absatz oder Stil definiert wurden. Die Sammlung enthält keine Tabulatoren, die in den übergeordneten Stilen oder als Standard‑Tabulatoren definiert sind.

## Beispiele



Zeigt, wie man mit der Tabulatorsammlung eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 Punkte entsprechen einem "Zoll" auf der Tabulatorlineal von Microsoft Word.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Jedes "Tab"‑Zeichen bewegt den Cursor des Builders zur Position des nächsten Tabulators.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Jeder Absatz erhält seine Tabulatorsammlung, die ihre Werte aus der Tabulatorsammlung des Dokument‑Builders kopiert.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// Eine Tabstoppsammlung kann uns zu TabStops vor und nach bestimmten Positionen führen.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Wir können die Tabstoppsammlung eines Absatzes löschen, um zum Standard-Tab-Verhalten zurückzukehren.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## Siehe auch

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
