---
title: "Aspose::Words::DocumentBuilder::InsertOleObject Methode"
linktitle: "InsertOleObject"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertOleObject Methode. Fügt ein eingebettetes OLE-Objekt aus einem Stream in das Dokument in C++ ein."
type: docs
weight: 41000
url: /de/cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Fügt ein eingebettetes OLE‑Objekt aus einem Stream in das Dokument ein.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Stream, der Anwendungsdaten enthält. |
| progId | const System::String\& | Programmierbarer Bezeichner des OLE-Objekts. |
| asIcon | bool | Gibt entweder den ikonischen oder den normalen Modus des einzufügenden OLE-Objekts an. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Bilddarstellung des OLE-Objekts. Wenn der Wert **null** ist, verwendet Aspose.Words eines der vordefinierten Bilder. |

### ReturnValue

Shape‑Knoten, der ein Ole‑Objekt enthält und an der aktuellen Builder‑Position eingefügt wird.

## Beispiele



Zeigt, wie man den DocumentBuilder verwendet, um OLE-Objekte in ein Dokument einzubetten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Microsoft Excel-Tabelle aus dem lokalen Dateisystem ein
// in das Dokument ein, wobei das Standardaussehen beibehalten wird.
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode
    // das Symbol gemäß 'progId' aus und verwendet die vordefinierte Symbolbeschriftung.
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// Fügen Sie eine Microsoft PowerPoint-Präsentation als OLE-Objekt ein.
// Dieses Mal wird es ein aus dem Web heruntergeladenes Bild als Symbol haben.
{
    System::SharedPtr<System::IO::Stream> powerpointStream = System::IO::File::Open(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    System::ArrayPtr<uint8_t> imgBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

    {
        auto imageStream = System::MakeObject<System::IO::MemoryStream>(imgBytes);
        builder->InsertParagraph();
        builder->Writeln(u"Powerpoint Ole object:");
        builder->InsertOleObject(powerpointStream, u"OleObject.pptx", true, imageStream);
    }
}

// Doppelklicken Sie diese Objekte in Microsoft Word, um zu öffnen
// die verknüpften Dateien mit den jeweiligen Anwendungen.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Fügt ein eingebettetes oder verknüpftes OLE‑Objekt aus einer Datei in das Dokument ein. Erkennt den OLE‑Objekttyp anhand der Dateierweiterung.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Vollständiger Pfad zur Datei. |
| isLinked | bool | Wenn **true** dann wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| asIcon | bool | Gibt entweder den ikonischen oder den normalen Modus des einzufügenden OLE-Objekts an. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Bilddarstellung des OLE-Objekts. Wenn der Wert **null** ist, verwendet Aspose.Words eines der vordefinierten Bilder. |

### ReturnValue

Shape‑Knoten, der ein Ole‑Objekt enthält und an der aktuellen Builder‑Position eingefügt wird.

## Beispiele



Zeigt, wie man ein OLE-Objekt in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE-Objekte sind Verknüpfungen zu Dateien in unserem lokalen Dateisystem, die von anderen installierten Anwendungen geöffnet werden können.
// Durch Doppelklicken auf diese Formen wird die Anwendung gestartet und anschließend zum Öffnen des verknüpften Objekts verwendet.
// Es gibt drei Möglichkeiten, die InsertOleObject-Methode zu verwenden, um diese Formen einzufügen und ihr Aussehen zu konfigurieren.
// 1 - Bild aus dem lokalen Dateisystem:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode
    // das Symbol gemäß der Dateierweiterung aus und verwendet den Dateinamen für die Symbolbeschriftung.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode
// das Symbol gemäß 'progId' aus und verwendet den Dateinamen für die Symbolbeschriftung.
// 2 - Symbol basierend auf der Anwendung, die das Objekt öffnet:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
// das Symbol gemäß 'progId' aus und verwendet die vordefinierte Symbolbeschriftung.
// 3 - Bildsymbol, das 32 × 32 Pixel oder kleiner ist, aus dem lokalen Dateisystem, mit einer benutzerdefinierten Beschriftung:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Fügt ein eingebettetes oder verknüpftes OLE‑Objekt aus einer Datei in das Dokument ein. Erkennt den OLE‑Objekttyp anhand des angegebenen progID‑Parameters.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Vollständiger Pfad zur Datei. |
| progId | const System::String\& | ProgId des OLE-Objekts. |
| isLinked | bool | Wenn **true** dann wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| asIcon | bool | Gibt entweder den ikonischen oder den normalen Modus des einzufügenden OLE-Objekts an. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Bilddarstellung des OLE-Objekts. Wenn der Wert **null** ist, verwendet Aspose.Words eines der vordefinierten Bilder. |

### ReturnValue

Shape‑Knoten, der ein Ole‑Objekt enthält und an der aktuellen Builder‑Position eingefügt wird.

## Beispiele



Zeigt, wie man ein OLE-Objekt in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE-Objekte sind Verknüpfungen zu Dateien in unserem lokalen Dateisystem, die von anderen installierten Anwendungen geöffnet werden können.
// Durch Doppelklicken auf diese Formen wird die Anwendung gestartet und anschließend zum Öffnen des verknüpften Objekts verwendet.
// Es gibt drei Möglichkeiten, die InsertOleObject-Methode zu verwenden, um diese Formen einzufügen und ihr Aussehen zu konfigurieren.
// 1 - Bild aus dem lokalen Dateisystem:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode
    // das Symbol gemäß der Dateierweiterung aus und verwendet den Dateinamen für die Symbolbeschriftung.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode
// das Symbol gemäß 'progId' aus und verwendet den Dateinamen für die Symbolbeschriftung.
// 2 - Symbol basierend auf der Anwendung, die das Objekt öffnet:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
// das Symbol gemäß 'progId' aus und verwendet die vordefinierte Symbolbeschriftung.
// 3 - Bildsymbol, das 32 × 32 Pixel oder kleiner ist, aus dem lokalen Dateisystem, mit einer benutzerdefinierten Beschriftung:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
