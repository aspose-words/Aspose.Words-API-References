---
title: "Aspose::Words::Fields::FieldEnd Klasse"
linktitle: "FieldEnd"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldEnd Klasse. Stellt das Ende eines Word-Feldes in einem Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 39000
url: /de/cpp/aspose.words.fields/fieldend/
---
## FieldEnd class


Stellt das Ende eines Word-Felds in einem Dokument dar. Weitere Informationen finden Sie im [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldEnd : public Aspose::Words::Fields::FieldChar
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_FieldType](../fieldchar/get_fieldtype/)() const | Gibt den Typ des Feldes zurück. |
| [get_Font](../../aspose.words/inline/get_font/)() | Stellt Zugriff auf die Schriftformatierung dieses Objekts bereit. |
| [get_HasSeparator](./get_hasseparator/)() const | Gibt **true** zurück, wenn dieses Feld einen Trenner hat. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Liefert **true**, wenn dieser Knoten andere Knoten enthalten kann. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsDirty](../fieldchar/get_isdirty/)() const | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsLocked](../fieldchar/get_islocked/)() const | Liest oder setzt, ob das übergeordnete Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [FieldEnd](../../aspose.words/nodetype/) zurück. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Ruft den übergeordneten [Paragraph](../../aspose.words/paragraph/) dieses Knotens ab. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Gibt ein [Range](../../aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](../fieldchar/getfield/)() | Gibt ein Feld für das Feldzeichen zurück. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Liefert das Sonderzeichen, das dieser Knoten darstellt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsDirty](../fieldchar/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::FieldChar::get_IsDirty](../fieldchar/get_isdirty/). |
| [set_IsLocked](../fieldchar/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::FieldChar::get_IsLocked](../fieldchar/get_islocked/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


[FieldEnd](./) is an inline-level node and represented by the [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) control character in the document.

[FieldEnd](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

Ein vollständiges Feld in einem Microsoft Word-Dokument ist eine komplexe Struktur, die aus einem Feldstartzeichen, Feldcode, Feldtrennzeichen, Feldresultat und Feldendzeichen besteht. Einige Felder haben nur Feldstart, Feldcode und Feldende.

Um ein neues Feld einfach in ein Dokument einzufügen, verwenden Sie die Methode [InsertField()](../).
## Siehe auch

* Class [FieldChar](../fieldchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
