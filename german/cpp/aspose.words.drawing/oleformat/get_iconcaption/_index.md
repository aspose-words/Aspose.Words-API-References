---
title: "Aspose::Words::Drawing::OleFormat::get_IconCaption Methode"
linktitle: "get_IconCaption"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::OleFormat::get_IconCaption Methode. Gibt die Symbolbeschriftung des OLE-Objekts zurück. Falls das OLE-Objekt kein Symbol hat oder die Beschriftung nicht abgerufen werden kann, wird in C++ eine leere Zeichenfolge zurückgegeben."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing/oleformat/get_iconcaption/
---
## OleFormat::get_IconCaption method


Liest die Symbolbeschriftung des OLE-Objekts. Falls das OLE-Objekt kein Symbol hat oder die Beschriftung nicht abgerufen werden kann, wird ein leerer String zurückgegeben.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_IconCaption()
```


## Beispiele



Zeigt, wie man verknüpfte und nicht verknüpfte OLE-Objekte einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Betten Sie eine Microsoft Visio-Zeichnung als OLE-Objekt in das Dokument ein.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// Fügen Sie einen Link zur Datei im lokalen Dateisystem ein und zeigen Sie ihn als Symbol an.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// Das Einfügen von OLE-Objekten erzeugt Formen, die diese Objekte speichern.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());
ASSERT_EQ(2, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::OleObject;
}))));

// Wenn eine Form ein OLE-Objekt enthält, hat sie eine gültige \"OleFormat\"‑Eigenschaft,
// die wir verwenden können, um einige Aspekte der Form zu überprüfen.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(false, oleFormat->get_OleIcon());

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(true, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(true, oleFormat->get_OleIcon());

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(u"", oleFormat->get_SourceItem());

ASSERT_EQ(u"Microsoft Visio drawing.vsd", oleFormat->get_IconCaption());

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// Wenn das Objekt OLE-Daten enthält, können wir über einen Stream darauf zugreifen.
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(76, oleEntryBytes->get_Length());
}
```

## Siehe auch

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
