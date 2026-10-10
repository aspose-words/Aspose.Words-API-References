---
title: "Aspose::Words::SectionCollection Klasse"
linktitle: "SectionCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::SectionCollection Klasse. Eine Sammlung von Section-Objekten im Dokument. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 59000
url: /de/cpp/aspose.words/sectioncollection/
---
## SectionCollection class


Eine Sammlung von [Section](../section/) Objekten im Dokument. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten am Ende der Sammlung hinzu. |
| [Clear](../nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bestimmt, ob ein Knoten in der Sammlung ist. |
| [get_Count](../nodecollection/get_count/)() | Ermittelt die Anzahl der Knoten in der Sammlung. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Bietet eine einfache \"foreach\"-artige Iteration über die Sammlung von Knoten. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ruft einen Abschnitt am angegebenen Index ab. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten in die Sammlung am angegebenen Index ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](./toarray/)() | Kopiert alle Abschnitte aus der Sammlung in ein neues Array von Abschnitten. |
| static [Type](./type/)() |  |
## Hinweise


Ein Microsoft‑Word‑Dokument kann mehrere Abschnitte enthalten. Um einen Abschnitt in Microsoft Word zu erstellen, wählen Sie den Befehl Einfügen/Umbruch und wählen Sie einen Umbruchtyp aus. Der Umbruch legt fest, ob der Abschnitt auf einer neuen Seite oder auf derselben Seite beginnt.

Das programmgesteuerte Einfügen und Entfernen von Abschnitten kann verwendet werden, um Dokumente, die beim Seriendruck erstellt werden, anzupassen. Wenn ein Dokument je nach Kriterien unterschiedliche Inhalte oder Teile davon enthalten muss, können Sie ein "Master"-Dokument erstellen, das mehrere Abschnitte enthält, und einige der Abschnitte vor oder nach dem Seriendruck löschen.

## Beispiele



Zeigt, wie man Abschnitte in einem Dokument hinzufügt und entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Löschen Sie den ersten Abschnitt aus dem Dokument.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Fügen Sie eine Kopie des jetzt ersten Abschnitts am Ende des Dokuments an.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Siehe auch

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
