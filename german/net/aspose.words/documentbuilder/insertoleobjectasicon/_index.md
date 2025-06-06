---
title: DocumentBuilder.InsertOleObjectAsIcon
linktitle: InsertOleObjectAsIcon
articleTitle: InsertOleObjectAsIcon
second_title: Aspose.Words für .NET
description: Fügen Sie mit DocumentBuilder mühelos OLE-Objekte als Symbole in Ihre Dokumente ein. Passen Sie Symbole und Beschriftungen an und sorgen Sie für eine nahtlose Integration.
type: docs
weight: 430
url: /de/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(*string, bool, string, string*) {#insertoleobjectasicon_1}

Fügt ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument ein. Ermöglicht die Angabe der Symboldatei und der Beschriftung. Erkennt den OLE-Objekttyp anhand der Dateierweiterung.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Vollständiger Pfad zur Datei. |
| isLinked | Boolean | Wenn`WAHR` dann wird das verknüpfte OLE-Objekt eingefügt, andernfalls wird das eingebettete OLE-Objekt eingefügt. |
| iconFile | String | Vollständiger Pfad zur ICO-Datei. Wenn der Wert`null` , Aspose.Words verwendet ein vordefiniertes Bild. |
| iconCaption | String | Symbolbeschriftung. Wenn der Wert`null` , Aspose.Words verwendet den Dateinamen. |

### Rückgabewert

Formknoten, der ein OLE-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

## Beispiele

Zeigt, wie ein OLE-Objekt in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-Objekte sind Links zu Dateien in unserem lokalen Dateisystem, die von anderen installierten Anwendungen geöffnet werden können.
// Durch Doppelklicken auf diese Formen wird die Anwendung gestartet und anschließend das verknüpfte Objekt geöffnet.
// Es gibt drei Möglichkeiten, diese Formen mit der Methode InsertOleObject einzufügen und ihr Erscheinungsbild zu konfigurieren.
// 1 - Bild aus dem lokalen Dateisystem entnommen:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Wenn 'presentation' weggelassen und 'asIcon' gesetzt ist, wählt diese überladene Methode
    // das Symbol entsprechend der Dateierweiterung und verwendet den Dateinamen für die Symbolbeschriftung.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Wenn 'presentation' weggelassen und 'asIcon' gesetzt ist, wählt diese überladene Methode
// das Symbol gemäß „progId“ und verwendet den Dateinamen für die Symbolbeschriftung.
// 2 – Symbol basierend auf der Anwendung, die das Objekt öffnet:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
// das Symbol entsprechend „progId“ und verwendet die vordefinierte Symbolbeschriftung.
// 3 – Bildsymbol mit 32 x 32 Pixeln oder kleiner aus dem lokalen Dateisystem, mit einer benutzerdefinierten Beschriftung:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*string, string, bool, string, string*) {#insertoleobjectasicon_2}

Fügt ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument ein. Ermöglicht die Angabe der Symboldatei und der Beschriftung. Erkennt den OLE-Objekttyp anhand des angegebenen progID-Parameters.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Vollständiger Pfad zur Datei. |
| progId | String | ProgId des OLE-Objekts. |
| isLinked | Boolean | Wenn`WAHR` dann wird das verknüpfte OLE-Objekt eingefügt, andernfalls wird das eingebettete OLE-Objekt eingefügt. |
| iconFile | String | Vollständiger Pfad zur ICO-Datei. Wenn der Wert`null` , Aspose.Words verwendet ein vordefiniertes Bild. |
| iconCaption | String | Symbolbeschriftung. Wenn der Wert`null` , Aspose.Words verwendet den Dateinamen. |

### Rückgabewert

Formknoten, der ein OLE-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

## Beispiele

Zeigt, wie ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
// das Symbol gemäß „progId“ und verwendet den Dateinamen für die Symbolbeschriftung.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
    // das Symbol entsprechend der Dateierweiterung und verwendet den Dateinamen für die Symbolbeschriftung.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*Stream, string, string, string*) {#insertoleobjectasicon}

Fügt ein eingebettetes OLE-Objekt als Symbol aus einem Stream in das Dokument ein. Ermöglicht die Angabe der Symboldatei und der Beschriftung. Erkennt den OLE-Objekttyp anhand des angegebenen progID-Parameters.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Stream mit Anwendungsdaten. |
| progId | String | ProgId des OLE-Objekts. |
| iconFile | String | Vollständiger Pfad zur ICO-Datei. Wenn der Wert`null` , Aspose.Words verwendet ein vordefiniertes Bild. |
| iconCaption | String | Symbolbeschriftung. Wenn der Wert`null` , Aspose.Words verwendet eine vordefinierte Symbolbeschriftung. |

### Rückgabewert

Formknoten, der ein OLE-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

## Beispiele

Zeigt, wie ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
// das Symbol gemäß „progId“ und verwendet den Dateinamen für die Symbolbeschriftung.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
    // das Symbol entsprechend der Dateierweiterung und verwendet den Dateinamen für die Symbolbeschriftung.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
