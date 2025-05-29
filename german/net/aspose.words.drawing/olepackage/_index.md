---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words für .NET
description: Erkunden Sie die Klasse Aspose.Words.Drawing.OlePackage, um OLE-Paketeigenschaften einfach zu verwalten und Ihre Dokumentverarbeitungsfunktionen zu verbessern.
type: docs
weight: 1540
url: /de/net/aspose.words.drawing/olepackage/
---
## OlePackage class

Ermöglicht den Zugriff auf OLE-Paketeigenschaften.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit OLE-Objekten](https://docs.aspose.com/words/net/working-with-ole-objects/) Dokumentationsartikel.

```csharp
public class OlePackage
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | Ruft den Anzeigenamen des OLE-Pakets ab oder legt ihn fest. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | Ruft den Dateinamen des OLE-Pakets ab oder legt ihn fest. |

## Bemerkungen

OLE-Pakete sind eine veraltete und „undokumentierte“ Methode zum Speichern eingebetteter Objekte, wenn der OLE-Handler unbekannt ist. Frühe Windows-Versionen wie Windows 3.1, 95 und 98 verfügten über die Anwendung Packager.exe, mit der beliebige Datentypen in Dokumente eingebettet werden konnten. Diese Anwendung ist mittlerweile nicht mehr in Windows enthalten, wird aber von MS Word und anderen Anwendungen weiterhin zum Einbetten von Daten verwendet, wenn der OLE-Handler fehlt oder unbekannt ist.

## Beispiele

Zeigt, wie ein OLE-Objekt in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-Objekte ermöglichen es uns, andere Dateien im lokalen Dateisystem mit einer anderen installierten Anwendung zu öffnen
// in unserem Betriebssystem durch Doppelklicken auf die Form, die das OLE-Objekt im Dokumenttext enthält.
// In diesem Fall ist unsere externe Datei ein ZIP-Archiv.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
