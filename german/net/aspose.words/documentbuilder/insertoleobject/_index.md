---
title: DocumentBuilder.InsertOleObject
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt ein eingebettetes OLEObjekt aus einem Stream in das Dokument ein.
type: docs
weight: 400
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
| presentation | Stream | Bildpräsentation des OLE-Objekts. Wenn Wert ist`Null` Aspose.Words verwendet eines der vordefinierten Bilder. |

### Rückgabewert

Formknoten, der das Ole-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

### Beispiele

Zeigt, wie Sie mit dem Document Builder OLE-Objekte in ein Dokument einbetten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Microsoft Excel-Tabelle aus dem lokalen Dateisystem einfügen
// in das Dokument einfügen und dabei sein Standard-Erscheinungsbild beibehalten.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // Wenn 'presentation' weggelassen und 'asIcon' gesetzt ist, wählt diese überladene Methode aus
    // das Icon gemäß 'progId' und verwendet die vordefinierte Icon-Beschriftung.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Eine Microsoft Powerpoint-Präsentation als OLE-Objekt einfügen.
// Dieses Mal wird ein Bild aus dem Internet für ein Symbol heruntergeladen.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (HttpClient httpClient = new HttpClient())
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
| isLinked | Boolean | Wenn`WAHR` Dann wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| asIcon | Boolean | Gibt entweder den ikonischen oder den normalen Modus des einzufügenden OLE-Objekts an. |
| presentation | Stream | Bildpräsentation des OLE-Objekts. Wenn Wert ist`Null` Aspose.Words verwendet eines der vordefinierten Bilder. |

### Rückgabewert

Formknoten, der das Ole-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

### Beispiele

Zeigt, wie ein OLE-Objekt in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-Objekte sind Links zu Dateien in unserem lokalen Dateisystem, die von anderen installierten Anwendungen geöffnet werden können.
// Durch Doppelklicken auf diese Formen wird die Anwendung gestartet und dann zum Öffnen des verknüpften Objekts verwendet.
// Es gibt drei Möglichkeiten, die InsertOleObject-Methode zum Einfügen dieser Formen und zum Konfigurieren ihres Erscheinungsbilds zu verwenden.
// 1 – Bild aus dem lokalen Dateisystem:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Wenn 'presentation' weggelassen und 'asIcon' gesetzt ist, wählt diese überladene Methode aus
    // das Symbol entsprechend der Dateierweiterung und verwendet den Dateinamen für die Symbolbeschriftung.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Wenn 'presentation' weggelassen und 'asIcon' gesetzt ist, wählt diese überladene Methode aus
// das Symbol gemäß „progId“ und verwendet den Dateinamen für die Symbolbeschriftung.
// 2 – Symbol basierend auf der Anwendung, die das Objekt öffnet:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode aus
// das Icon gemäß 'progId' und verwendet die vordefinierte Icon-Beschriftung.
// 3 – Bildsymbol, das 32 x 32 Pixel oder kleiner ist, aus dem lokalen Dateisystem, mit einer benutzerdefinierten Beschriftung:
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

Fügt ein eingebettetes oder verknüpftes OLE-Objekt aus einer Datei in das Dokument ein. Erkennt den OLE-Objekttyp mithilfe des angegebenen progID-Parameters.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Vollständiger Pfad zur Datei. |
| progId | String | ProgId des OLE-Objekts. |
| isLinked | Boolean | Wenn`WAHR` Dann wird ein verknüpftes OLE-Objekt eingefügt, andernfalls wird ein eingebettetes OLE-Objekt eingefügt. |
| asIcon | Boolean | Gibt entweder den ikonischen oder den normalen Modus des einzufügenden OLE-Objekts an. |
| presentation | Stream | Bildpräsentation des OLE-Objekts. Wenn Wert ist`Null` Aspose.Words verwendet eines der vordefinierten Bilder. |

### Rückgabewert

Formknoten, der das Ole-Objekt enthält und an der aktuellen Builder-Position eingefügt wird.

### Beispiele

Zeigt, wie ein OLE-Objekt in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-Objekte sind Links zu Dateien in unserem lokalen Dateisystem, die von anderen installierten Anwendungen geöffnet werden können.
// Durch Doppelklicken auf diese Formen wird die Anwendung gestartet und dann zum Öffnen des verknüpften Objekts verwendet.
// Es gibt drei Möglichkeiten, die InsertOleObject-Methode zum Einfügen dieser Formen und zum Konfigurieren ihres Erscheinungsbilds zu verwenden.
// 1 – Bild aus dem lokalen Dateisystem:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Wenn 'presentation' weggelassen und 'asIcon' gesetzt ist, wählt diese überladene Methode aus
    // das Symbol entsprechend der Dateierweiterung und verwendet den Dateinamen für die Symbolbeschriftung.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Wenn 'presentation' weggelassen und 'asIcon' gesetzt ist, wählt diese überladene Methode aus
// das Symbol gemäß „progId“ und verwendet den Dateinamen für die Symbolbeschriftung.
// 2 – Symbol basierend auf der Anwendung, die das Objekt öffnet:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode aus
// das Icon gemäß 'progId' und verwendet die vordefinierte Icon-Beschriftung.
// 3 – Bildsymbol, das 32 x 32 Pixel oder kleiner ist, aus dem lokalen Dateisystem, mit einer benutzerdefinierten Beschriftung:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


