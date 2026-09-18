---
title: "Aspose::Words::Range Klasse"
linktitle: "Range"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Range Klasse. Stellt einen zusammenhängenden Bereich in einem Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 51000
url: /de/cpp/aspose.words/range/
---
## Range class


Stellt einen zusammenhängenden Bereich in einem Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/).

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Delete](./delete/)() | Löscht alle Zeichen des Bereichs. |
| [get_Bookmarks](./get_bookmarks/)() | Gibt eine [Bookmarks](./get_bookmarks/) Sammlung zurück, die alle Lesezeichen im Bereich darstellt. |
| [get_Fields](./get_fields/)() | Gibt eine [Fields](./get_fields/) Sammlung zurück, die alle Felder im Bereich darstellt. |
| [get_FormFields](./get_formfields/)() | Gibt eine [FormFields](./get_formfields/) Sammlung zurück, die alle Formularfelder im Bereich darstellt. |
| [get_Revisions](./get_revisions/)() | Ruft eine Sammlung von Revisionen (nachverfolgte Änderungen) ab, die in diesem Bereich existieren. |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | Gibt eine [StructuredDocumentTags](./get_structureddocumenttags/) Sammlung zurück, die alle strukturierten Dokument-Tags im Bereich darstellt. |
| [get_Text](./get_text/)() | Ruft den Text des Bereichs ab. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Ändert die Feldtypwerte [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) von [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/) und [FieldEnd](../../aspose.words.fields/fieldend/) in diesem Bereich, sodass sie den im Feldcode enthaltenen Feldtypen entsprechen. |
| [Replace](./replace/)(const System::String\&, const System::String\&) | Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Ersetzt alle Vorkommen eines durch einen regulären Ausdruck angegebenen Zeichenmusters durch eine andere Zeichenfolge. |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Ersetzt alle Vorkommen eines durch einen regulären Ausdruck angegebenen Zeichenmusters durch eine andere Zeichenfolge. |
| [ToDocument](./todocument/)() | Erstellt ein neues vollständig aufgebautes Dokument, das den Bereich enthält. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Löst die Verknüpfung von Feldern in diesem Bereich. |
| [UpdateFields](./updatefields/)() | Aktualisiert die Werte von Dokumentfeldern in diesem Bereich. |
## Hinweise


Das Dokument wird durch einen Knotenbaum dargestellt, und die Knoten bieten Operationen zur Arbeit mit dem Baum, jedoch sind einige Vorgänge einfacher auszuführen, wenn das Dokument als zusammenhängende Textsequenz behandelt wird.

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## Beispiele



Zeigt, wie man den Textinhalt aller Knoten abruft, die von einem Bereich abgedeckt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
