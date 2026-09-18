---
title: "Aspose::Words::Layout::LayoutEnumerator Klasse"
linktitle: "LayoutEnumerator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutEnumerator Klasse. Enumeriert Layout-Entitäten einer Seite eines Dokuments. Sie können diese Klasse verwenden, um das Seitenlayout‑Modell zu durchlaufen. Verfügbare Eigenschaften sind Typ, Geometrie, Text und Seitenindex, an dem die Entität gerendert wird, sowie die Gesamtstruktur und Beziehungen. Verwenden Sie die Kombination von GetEntity() und Current, um zur Entität zu wechseln, die einem Dokumentknoten entspricht. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


Enumeriert Layout-Entitäten einer Seite eines Dokuments. Sie können diese Klasse verwenden, um das Seitenlayout‑Modell zu durchlaufen. Verfügbare Eigenschaften sind Typ, Geometrie, Text und Seitenindex, an dem die Entität gerendert wird, sowie die Gesamtstruktur und Beziehungen. Verwenden Sie die Kombination von [GetEntity()](../) und [Current](./get_current/), um zur Entität zu wechseln, die einem Dokumentknoten entspricht. Weitere Informationen finden Sie im Dokumentationsartikel [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | Liest oder setzt die aktuelle Position im Seitenlayout‑Modell. Diese Eigenschaft gibt ein undurchsichtiges Objekt zurück, das der aktuellen Layout‑Entität entspricht. |
| [get_Document](./get_document/)() const | Liest das Dokument, das diese Instanz enumeriert. |
| [get_Kind](./get_kind/)() | Liest die Art der aktuellen Entität. Dies kann eine leere Zeichenkette sein, aber niemals **null**. |
| [get_PageIndex](./get_pageindex/)() | Liest den 1‑basierten Index einer Seite, die die aktuelle Entität enthält. |
| [get_Rectangle](./get_rectangle/)() | Gibt das Begrenzungsrechteck der aktuellen Entität relativ zur oberen linken Ecke der Seite zurück (in Punkten). |
| [get_Text](./get_text/)() | Liest den Text der aktuellen Span‑Entität. Wirft bei anderen Entitätstypen. |
| [get_Type](./get_type/)() | Liest den Typ der aktuellen Entität. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Liest eine benannte Eigenschaft der Entität. |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initialisiert eine neue Instanz dieser Klasse. |
| [MoveFirstChild](./movefirstchild/)() | Wechselt zur ersten Kind‑Entität. |
| [MoveLastChild](./movelastchild/)() | Wechselt zur letzten Kind‑Entität. |
| [MoveNext](./movenext/)() | Wechselt zur nächsten Geschwister‑Entität in visueller Reihenfolge. Beim Durchlaufen von Zeilen eines Absatzes, der über mehrere Seiten hinweg gebrochen ist, springt diese Methode nicht zur nächsten Seite, sondern zur nächsten Entität auf derselben Seite. |
| [MoveNextLogical](./movenextlogical/)() | Wechselt zur nächsten Geschwister‑Entität in logischer Reihenfolge. Beim Durchlaufen von Zeilen eines Absatzes, der über mehrere Seiten hinweg gebrochen ist, springt diese Methode zur nächsten Zeile, selbst wenn sie sich auf einer anderen Seite befindet. |
| [MoveParent](./moveparent/)() | Wechselt zur übergeordneten Entität. |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | Wechselt zur übergeordneten Entität des angegebenen Typs. |
| [MovePrevious](./moveprevious/)() | Wechselt zur vorherigen Geschwister‑Entität. |
| [MovePreviousLogical](./movepreviouslogical/)() | Wechselt zur vorherigen Geschwister‑Entität in logischer Reihenfolge. Beim Durchlaufen von Zeilen eines Absatzes, der über mehrere Seiten hinweg gebrochen ist, springt diese Methode zur vorherigen Zeile, selbst wenn sie sich auf einer anderen Seite befindet. |
| [Reset](./reset/)() | Wechselt den Enumerator zur ersten Seite des Dokuments. |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | Setter für [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/). |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
