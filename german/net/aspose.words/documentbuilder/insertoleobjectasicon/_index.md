---
title: InsertOleObjectAsIcon
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument ein. Ermöglicht die Angabe von Symboldatei und Beschriftung. Erkennt den OLE-Objekttyp anhand der Dateierweiterung.
type: docs
weight: 380
url: /de/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(string, bool, string, string) {#insertoleobjectasicon_1}

Fügt ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument ein. Ermöglicht die Angabe von Symboldatei und Beschriftung. Erkennt den OLE-Objekttyp anhand der Dateierweiterung.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Vollständiger Pfad zur Datei. |
| isLinked | Boolean | Wenn wahr, wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| iconFile | String | Vollständiger Pfad zur ICO-Datei. Wenn der Wert null ist, verwendet Aspose.Words ein vordefiniertes Bild. |
| iconCaption | String | Symbolbeschriftung. Wenn der Wert null ist, verwendet Aspose.Words den Dateinamen. |

### Rückgabewert

Shape-Knoten, der das Ole-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

### Beispiele

Zeigt, wie ein OLE-Objekt in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-Objekte sind Links zu Dateien in unserem lokalen Dateisystem, die von anderen installierten Anwendungen geöffnet werden können.
// Ein Doppelklick auf diese Formen startet die Anwendung und verwendet sie dann, um das verknüpfte Objekt zu öffnen.
// Es gibt drei Möglichkeiten, die InsertOleObject-Methode zu verwenden, um diese Formen einzufügen und ihr Aussehen zu konfigurieren.
// 1 - Image aus dem lokalen Dateisystem:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode aus
    // das Icon entsprechend der Dateiendung und verwendet den Dateinamen für die Icon-Beschriftung.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode aus
// das Icon gemäß 'progId' und verwendet den Dateinamen für die Icon-Beschriftung.
// 2 - Symbol basierend auf der Anwendung, die das Objekt öffnet:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode aus
// das Icon gemäß 'progId' und verwendet die vordefinierte Icon-Beschriftung.
// 3 - Bildsymbol, das 32 x 32 Pixel oder kleiner aus dem lokalen Dateisystem ist, mit einer benutzerdefinierten Beschriftung:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(string, string, bool, string, string) {#insertoleobjectasicon_2}

Fügt ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument ein. Ermöglicht die Angabe von Symboldatei und Beschriftung. Erkennt den OLE-Objekttyp anhand des angegebenen progID-Parameters.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Vollständiger Pfad zur Datei. |
| progId | String | ProgId des OLE-Objekts. |
| isLinked | Boolean | Wenn wahr, wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| iconFile | String | Vollständiger Pfad zur ICO-Datei. Wenn der Wert null ist, verwendet Aspose.Words ein vordefiniertes Bild. |
| iconCaption | String | Symbolbeschriftung. Wenn der Wert null ist, verwendet Aspose.Words den Dateinamen. |

### Rückgabewert

Shape-Knoten, der das Ole-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

### Beispiele

Zeigt, wie Sie ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode aus
// das Icon gemäß 'progId' und verwendet den Dateinamen für die Icon-Beschriftung.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode aus
    // das Icon entsprechend der Dateiendung und verwendet den Dateinamen für die Icon-Beschriftung.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(Stream, string, string, string) {#insertoleobjectasicon}

Fügt ein eingebettetes OLE-Objekt als Symbol aus einem Stream in das Dokument ein. Ermöglicht die Angabe von Symboldatei und Beschriftung. Erkennt den OLE-Objekttyp anhand des angegebenen progID-Parameters.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Stream mit Anwendungsdaten. |
| progId | String | ProgId des OLE-Objekts. |
| iconFile | String | Vollständiger Pfad zur ICO-Datei. Wenn der Wert null ist, verwendet Aspose.Words ein vordefiniertes Bild. |
| iconCaption | String | Symbolbeschriftung. Wenn der Wert null ist, verwendet Aspose.Words das vordefinierte Symbol caption. |

### Rückgabewert

Shape-Knoten, der das Ole-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

### Beispiele

Zeigt, wie Sie ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode aus
// das Icon gemäß 'progId' und verwendet den Dateinamen für die Icon-Beschriftung.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode aus
    // das Icon entsprechend der Dateiendung und verwendet den Dateinamen für die Icon-Beschriftung.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
