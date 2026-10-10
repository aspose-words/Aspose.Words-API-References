---
title: "Aspose::Words::TabStop Klasse"
linktitle: "TabStop"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TabStop class. Stellt einen einzelnen benutzerdefinierten Tabstopp dar. Das TabStop-Objekt ist ein Element der TabStopCollection-Sammlung. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 68000
url: /de/cpp/aspose.words/tabstop/
---
## TabStop class


Stellt einen einzelnen benutzerdefinierten Tabstopp dar. Das [TabStop](./)-Objekt ist ein Element der [TabStopCollection](../tabstopcollection/)-Sammlung. Weitere Informationen finden Sie im Dokumentationsartikel zum [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStop : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Vergleicht mit dem angegebenen [TabStop](./). |
| [get_Alignment](./get_alignment/)() const | Liest oder legt die Ausrichtung des Textes an diesem Tabstopp fest. |
| [get_IsClear](./get_isclear/)() | Gibt **true** zurück, wenn dieser Tabstopp vorhandene Tabstopps an dieser Position löscht. |
| [get_Leader](./get_leader/)() const | Liest oder legt den Typ der Führungszeichenlinie fest, die unter dem Tabulatorzeichen angezeigt wird. |
| [get_Position](./get_position/)() | Liest die Position des Tabstopps in Punkten. |
| [GetHashCode](./gethashcode/)() const override | Berechnet den Hashcode für dieses Objekt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | Setter für [Aspose::Words::TabStop::get_Alignment](./get_alignment/). |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | Setter für [Aspose::Words::TabStop::get_Leader](./get_leader/). |
| [TabStop](./tabstop/)(double) | Initialisiert eine neue Instanz dieser Klasse. |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Initialisiert eine neue Instanz dieser Klasse. |
| static [Type](./type/)() |  |
## Hinweise


Normalerweise gibt ein Tabstopp eine Position an, an der ein Tabstopp existiert. Da Tabstopps jedoch von übergeordneten Stilen vererbt werden können, muss das untergeordnete Objekt ggf. explizit festlegen, dass an einer bestimmten Position kein Tabstopp vorhanden ist. Um einen geerbten Tabstopp an einer bestimmten Position zu entfernen, erstellen Sie ein [TabStop](./)-Objekt und setzen Sie [Alignment](./get_alignment/) auf [Clear](../tabalignment/).

Weitere Informationen finden Sie unter [TabStopCollection](../tabstopcollection/).

## Beispiele



Zeigt, wie die Position des rechten Tabstopps in TOC‑bezogenen Absätzen geändert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// Durchlaufen Sie alle Absätze mit TOC‑ergebnisbasierten Stilen; das ist jeder Stil zwischen TOC und TOC9.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // Ermitteln Sie den ersten Tab, der in diesem Absatz verwendet wird; dies sollte der Tab sein, der zum Ausrichten der Seitenzahlen verwendet wird.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // Ersetzen Sie den ersten Standard‑Tabstopp durch einen benutzerdefinierten Tabstopp.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
