---
title: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon Methode"
linktitle: "InsertOleObjectAsIcon"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon Methode. Fügt ein eingebettetes OLE-Objekt als Symbol aus einem Stream in das Dokument ein. Ermöglicht die Angabe von Symboldatei und Beschriftung. Erkennt den OLE-Objekttyp anhand des angegebenen progID‑Parameters in C++."
type: docs
weight: 42000
url: /de/cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


Fügt ein eingebettetes OLE‑Objekt als Symbol aus einem Stream in das Dokument ein. Ermöglicht das Angeben einer Symboldatei und Beschriftung. Erkennt den OLE‑Objekttyp anhand des angegebenen progID‑Parameters.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Stream, der Anwendungsdaten enthält. |
| progId | const System::String\& | ProgId des OLE-Objekts. |
| iconFile | const System::String\& | Vollständiger Pfad zur ICO-Datei. Wenn der Wert **null** ist, verwendet Aspose.Words ein vordefiniertes Bild. |
| iconCaption | const System::String\& | Symbolbeschriftung. Wenn der Wert **null** ist, verwendet Aspose.Words eine vordefinierte Symbolbeschriftung. |

### ReturnValue

Shape‑Knoten, der ein Ole‑Objekt enthält und an der aktuellen Builder‑Position eingefügt wird.

## Beispiele



Zeigt, wie man ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
// das Symbol gemäß 'progId' aus und verwendet den Dateinamen für die Symbolbeschriftung.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
    // das Symbol gemäß der Dateierweiterung aus und verwendet den Dateinamen für die Symbolbeschriftung.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


Fügt ein eingebettetes oder verknüpftes OLE‑Objekt als Symbol in das Dokument ein. Ermöglicht das Angeben einer Symboldatei und Beschriftung. Erkennt den OLE‑Objekttyp anhand der Dateierweiterung.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Vollständiger Pfad zur Datei. |
| isLinked | bool | Wenn **true** dann wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| iconFile | const System::String\& | Vollständiger Pfad zur ICO-Datei. Wenn der Wert **null** ist, verwendet Aspose.Words ein vordefiniertes Bild. |
| iconCaption | const System::String\& | Symbolbeschriftung. Wenn der Wert **null** ist, verwendet Aspose.Words den Dateinamen. |

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
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


Fügt ein eingebettetes oder verknüpftes OLE‑Objekt als Symbol in das Dokument ein. Ermöglicht das Angeben einer Symboldatei und Beschriftung. Erkennt den OLE‑Objekttyp anhand des angegebenen progID‑Parameters.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Vollständiger Pfad zur Datei. |
| progId | const System::String\& | ProgId des OLE-Objekts. |
| isLinked | bool | Wenn **true** dann wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| iconFile | const System::String\& | Vollständiger Pfad zur ICO-Datei. Wenn der Wert **null** ist, verwendet Aspose.Words ein vordefiniertes Bild. |
| iconCaption | const System::String\& | Symbolbeschriftung. Wenn der Wert **null** ist, verwendet Aspose.Words den Dateinamen. |

### ReturnValue

Shape‑Knoten, der ein Ole‑Objekt enthält und an der aktuellen Builder‑Position eingefügt wird.

## Beispiele



Zeigt, wie man ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
// das Symbol gemäß 'progId' aus und verwendet den Dateinamen für die Symbolbeschriftung.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
    // das Symbol gemäß der Dateierweiterung aus und verwendet den Dateinamen für die Symbolbeschriftung.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
