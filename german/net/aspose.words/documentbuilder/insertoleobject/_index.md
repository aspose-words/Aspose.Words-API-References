---
title: InsertOleObject
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt ein eingebettetes OLEObjekt aus einem Stream in das Dokument ein.
type: docs
weight: 370
url: /de/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(Stream, string, bool, Stream) {#insertoleobject}

Fügt ein eingebettetes OLE-Objekt aus einem Stream in das Dokument ein.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Stream mit Anwendungsdaten. |
| progId | String | Programmatischer Bezeichner des OLE-Objekts. |
| asIcon | Boolean | Gibt entweder den ikonischen oder den normalen Modus des einzufügenden OLE-Objekts an. |
| presentation | Stream | Bilddarstellung des OLE-Objekts. Wenn der Wert null ist, verwendet Aspose.Words eines der vordefinierten Bilder. |

### Rückgabewert

Shape-Knoten, der das Ole-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

### Beispiele

Zeigt, wie Document Builder zum Einbetten von OLE-Objekten in ein Dokument verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Microsoft Excel-Tabelle aus dem lokalen Dateisystem einfügen
// in das Dokument unter Beibehaltung der Standarddarstellung.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode aus
    // das Icon gemäß 'progId' und verwendet die vordefinierte Icon-Beschriftung.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Eine Microsoft Powerpoint-Präsentation als OLE-Objekt einfügen.
// Diesmal wird ein Bild als Symbol aus dem Internet heruntergeladen.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (WebClient webClient = new WebClient())
    {
        byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

        using (MemoryStream imageStream = new MemoryStream(imgBytes))
        {
            builder.InsertParagraph();
            builder.Writeln("Powerpoint Ole object:");
            builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
        }
    }
}

// Doppelklicken Sie auf diese Objekte in Microsoft Word, um sie zu öffnen
// die verknüpften Dateien mit ihren jeweiligen Anwendungen.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertOleObject(string, bool, bool, Stream) {#insertoleobject_1}

Fügt ein eingebettetes oder verknüpftes OLE-Objekt aus einer Datei in das Dokument ein. Erkennt den OLE-Objekttyp anhand der Dateierweiterung.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Vollständiger Pfad zur Datei. |
| isLinked | Boolean | Wenn wahr, wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| asIcon | Boolean | Gibt entweder den ikonischen oder den normalen Modus des einzufügenden OLE-Objekts an. |
| presentation | Stream | Bilddarstellung des OLE-Objekts. Wenn der Wert null ist, verwendet Aspose.Words eines der vordefinierten Bilder. |

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertOleObject(string, string, bool, bool, Stream) {#insertoleobject_2}

Fügt ein eingebettetes oder verknüpftes OLE-Objekt aus einer Datei in das Dokument ein. Erkennt den OLE-Objekttyp anhand des angegebenen progID-Parameters.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Vollständiger Pfad zur Datei. |
| progId | String | ProgId des OLE-Objekts. |
| isLinked | Boolean | Wenn wahr, wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| asIcon | Boolean | Gibt entweder den ikonischen oder den normalen Modus des einzufügenden OLE-Objekts an. |
| presentation | Stream | Bilddarstellung des OLE-Objekts. Wenn der Wert null ist, verwendet Aspose.Words eines der vordefinierten Bilder. |

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
