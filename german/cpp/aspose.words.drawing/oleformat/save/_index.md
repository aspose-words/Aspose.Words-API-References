---
title: "Aspose::Words::Drawing::OleFormat::Save-Methode"
linktitle: "Save"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::OleFormat::Save-Methode. Speichert die Daten des eingebetteten Objekts in den angegebenen Stream in C++."
type: docs
weight: 19000
url: /de/cpp/aspose.words.drawing/oleformat/save/
---
## OleFormat::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Speichert die Daten des eingebetteten Objekts in den angegebenen Stream.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Wo die Objektdaten gespeichert werden sollen. |
## Hinweise


Es liegt in der Verantwortung des Aufrufers, den Stream zu entsorgen.

## Beispiele



Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// Das OLE-Objekt in der ersten Form ist eine Microsoft Excel-Tabelle.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Unser Objekt wird weder automatisch aktualisiert noch ist es vor Aktualisierungen gesperrt.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Wenn wir planen, das OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern,
// können wir die Eigenschaft "SuggestedExtension" verwenden, um zu bestimmen, welche Dateierweiterung auf die Datei angewendet werden soll.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Unten sind zwei Möglichkeiten, ein OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern.
// 1 -  Speichern Sie es über einen Stream:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Speichern Sie es direkt unter einem Dateinamen:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Siehe auch

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(const System::String\&) method


Speichert die Daten des eingebetteten Objekts in einer Datei mit dem angegebenen Namen.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Name der Datei, in der die OLE-Objektdaten gespeichert werden. |

## Beispiele



Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// Das OLE-Objekt in der ersten Form ist eine Microsoft Excel-Tabelle.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Unser Objekt wird weder automatisch aktualisiert noch ist es vor Aktualisierungen gesperrt.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Wenn wir planen, das OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern,
// können wir die Eigenschaft "SuggestedExtension" verwenden, um zu bestimmen, welche Dateierweiterung auf die Datei angewendet werden soll.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Unten sind zwei Möglichkeiten, ein OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern.
// 1 -  Speichern Sie es über einen Stream:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Speichern Sie es direkt unter einem Dateinamen:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Siehe auch

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::OleFormat::Save(std::basic_ostream<CharType, Traits> &stream)
```

## Siehe auch

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
