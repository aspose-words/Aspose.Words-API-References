---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.OlePackage klas. Ermöglicht den Zugriff auf OLEPaketeigenschaften in C#.
type: docs
weight: 1160
url: /de/net/aspose.words.drawing/olepackage/
---
## OlePackage class

Ermöglicht den Zugriff auf OLE-Paketeigenschaften.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Ole-Objekten](https://docs.aspose.com/words/net/working-with-ole-objects/) Dokumentationsartikel.

```csharp
public class OlePackage
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | Ruft den Anzeigenamen des OLE-Pakets ab oder legt diesen fest. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | Ruft den Namen der OLE-Paketdatei ab oder legt diesen fest. |

## Bemerkungen

OLE-Paket ist eine veraltete und „undokumentierte“ Methode zum Speichern eingebetteter Objekte, wenn der OLE-Handler unbekannt ist. Frühe Windows-Versionen wie Windows 3.1, 95 und 98 verfügten über die Anwendung Packager.exe, mit der beliebige Datentypen in Dokumente eingebettet werden konnten . Jetzt ist diese Anwendung von Windows ausgeschlossen, aber MS Word und andere Anwendungen verwenden sie weiterhin zum Einbetten von Daten, wenn der OLE-Handler fehlt oder unbekannt ist.

## Beispiele

Zeigt, wie ein OLE-Objekt in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-Objekte ermöglichen es uns, andere Dateien im lokalen Dateisystem mit einer anderen installierten Anwendung zu öffnen
// in unserem Betriebssystem durch Doppelklicken auf die Form, die das OLE-Objekt im Dokumentkörper enthält.
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
