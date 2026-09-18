---
title: "Aspose::Words::Drawing::OleFormat Klasse"
linktitle: "OleFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::OleFormat Klasse. Bietet Zugriff auf die Daten eines OLE-Objekts oder ActiveX-Steuerelements. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.drawing/oleformat/
---
## OleFormat class


Bietet Zugriff auf die Daten eines OLE-Objekts oder ActiveX-Steuerelements. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OleFormat : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Gibt an, ob die Verknüpfung zum OLE-Objekt in Microsoft Word automatisch aktualisiert wird oder nicht. |
| [get_Clsid](./get_clsid/)() | Liest die CLSID des OLE-Objekts. |
| [get_IconCaption](./get_iconcaption/)() | Liest die Symbolbeschriftung des OLE-Objekts. Falls das OLE-Objekt kein Symbol hat oder die Beschriftung nicht abgerufen werden kann, wird ein leerer String zurückgegeben. |
| [get_IsLink](./get_islink/)() | Gibt **true** zurück, wenn das OLE-Objekt verknüpft ist (wenn [SourceFullName](./get_sourcefullname/) angegeben ist). |
| [get_IsLocked](./get_islocked/)() | Gibt an, ob die Verknüpfung zum OLE-Objekt vor Aktualisierungen gesperrt ist. |
| [get_OleControl](./get_olecontrol/)() | Liest [OleControl](./get_olecontrol/)-Objekte, wenn dieses OLE-Objekt ein ActiveX-Steuerelement ist. Andernfalls ist diese Eigenschaft null. |
| [get_OleIcon](./get_oleicon/)() | Liest den Zeichenaspekt des OLE-Objekts. Wenn **true**, wird das OLE-Objekt als Symbol angezeigt. Wenn **false**, wird das OLE-Objekt als Inhalt angezeigt. |
| [get_OlePackage](./get_olepackage/)() | Stellt Zugriff auf [OlePackage](../olepackage/) bereit, wenn das OLE-Objekt ein OLE-Paket ist. Gibt sonst **null** zurück. |
| [get_ProgId](./get_progid/)() | Liest oder setzt die ProgID des OLE-Objekts. |
| [get_SourceFullName](./get_sourcefullname/)() | Liest oder setzt den Pfad und Namen der Quelldatei für das verknüpfte OLE-Objekt. |
| [get_SourceItem](./get_sourceitem/)() | Liest oder setzt einen String, der verwendet wird, um den Teil der Quelldatei zu identifizieren, der verknüpft wird. |
| [get_SuggestedExtension](./get_suggestedextension/)() | Liest die für das aktuelle eingebettete Objekt empfohlene Dateierweiterung, wenn Sie es in einer Datei speichern möchten. |
| [get_SuggestedFileName](./get_suggestedfilename/)() | Liest den für das aktuelle eingebettete Objekt empfohlenen Dateinamen, wenn Sie es in einer Datei speichern möchten. |
| [GetOleEntry](./getoleentry/)(const System::String\&) | Liest den Daten-Eintrag des OLE-Objekts. |
| [GetRawData](./getrawdata/)() | Liest die Rohdaten des OLE-Objekts. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Speichert die Daten des eingebetteten Objekts in den angegebenen Stream. |
| [Save](./save/)(const System::String\&) | Speichert die Daten des eingebetteten Objekts in einer Datei mit dem angegebenen Namen. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Setter für [Aspose::Words::Drawing::OleFormat::get_AutoUpdate](./get_autoupdate/). |
| [set_IsLocked](./set_islocked/)(bool) | Setter für [Aspose::Words::Drawing::OleFormat::get_IsLocked](./get_islocked/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Setter für [Aspose::Words::Drawing::OleFormat::get_ProgId](./get_progid/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Setter für [Aspose::Words::Drawing::OleFormat::get_SourceFullName](./get_sourcefullname/). |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Setter für [Aspose::Words::Drawing::OleFormat::get_SourceItem](./get_sourceitem/). |
| static [Type](./type/)() |  |
## Hinweise


Verwenden Sie die [OleFormat](../shape/get_oleformat/) Eigenschaft, um auf die Daten eines OLE-Objekts zuzugreifen. Sie erstellen keine Instanzen der [OleFormat](./) Klasse direkt.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
