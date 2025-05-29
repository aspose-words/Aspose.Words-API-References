---
title: DocumentBuilder.InsertOleObject
linktitle: InsertOleObject
articleTitle: InsertOleObject
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mühelos mit der InsertOleObject-Methode von DocumentBuilder, die das nahtlose Einbetten von OLE-Objekten aus Streams ermöglicht.
type: docs
weight: 420
url: /de/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(*Stream, string, bool, Stream*) {#insertoleobject}

Fügt ein eingebettetes OLE-Objekt aus einem Stream in das Dokument ein.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Stream mit Anwendungsdaten. |
| progId | String | Programmatische Kennung des OLE-Objekts. |
| asIcon | Boolean | Gibt entweder den Symbol- oder den Normalmodus des einzufügenden OLE-Objekts an. |
| presentation | Stream | Bilddarstellung des OLE-Objekts. Wenn der Wert`null` Aspose.Words verwendet eines der vordefinierten Bilder. |

### Rückgabewert

Formknoten, der ein OLE-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

## Beispiele

Zeigt, wie Sie mit dem Dokumentgenerator OLE-Objekte in ein Dokument einbetten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügt eine Microsoft Excel-Tabelle aus dem lokalen Dateisystem ein
// in das Dokument, während das Standardaussehen beibehalten wird.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // Wenn 'presentation' weggelassen und 'asIcon' gesetzt ist, wählt diese überladene Methode
    // das Symbol entsprechend „progId“ und verwendet die vordefinierte Symbolbeschriftung.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Fügen Sie eine Microsoft Powerpoint-Präsentation als OLE-Objekt ein.
// Dieses Mal wird als Symbol ein aus dem Internet heruntergeladenes Bild verwendet.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

    using (MemoryStream imageStream = new MemoryStream(imgBytes))
    {
        builder.InsertParagraph();
        builder.Writeln("Powerpoint Ole object:");
        builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
    }
}

// Doppelklicken Sie diese Objekte in Microsoft Word, um sie zu öffnen
// die verknüpften Dateien mithilfe ihrer jeweiligen Anwendungen.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertOleObject(*string, bool, bool, Stream*) {#insertoleobject_1}

Fügt ein eingebettetes oder verknüpftes OLE-Objekt aus einer Datei in das Dokument ein. Der OLE-Objekttyp wird anhand der Dateierweiterung erkannt.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Vollständiger Pfad zur Datei. |
| isLinked | Boolean | Wenn`WAHR`dann wird das verknüpfte OLE-Objekt eingefügt, andernfalls wird das eingebettete OLE-Objekt eingefügt. |
| asIcon | Boolean | Gibt entweder den Symbol- oder den Normalmodus des einzufügenden OLE-Objekts an. |
| presentation | Stream | Bilddarstellung des OLE-Objekts. Wenn der Wert`null` Aspose.Words verwendet eines der vordefinierten Bilder. |

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

## InsertOleObject(*string, string, bool, bool, Stream*) {#insertoleobject_2}

Fügt ein eingebettetes oder verknüpftes OLE-Objekt aus einer Datei in das Dokument ein. Der OLE-Objekttyp wird anhand des angegebenen progID-Parameters ermittelt.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Vollständiger Pfad zur Datei. |
| progId | String | ProgId des OLE-Objekts. |
| isLinked | Boolean | Wenn`WAHR`dann wird das verknüpfte OLE-Objekt eingefügt, andernfalls wird das eingebettete OLE-Objekt eingefügt. |
| asIcon | Boolean | Gibt entweder den Symbol- oder den Normalmodus des einzufügenden OLE-Objekts an. |
| presentation | Stream | Bilddarstellung des OLE-Objekts. Wenn der Wert`null` Aspose.Words verwendet eines der vordefinierten Bilder. |

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
