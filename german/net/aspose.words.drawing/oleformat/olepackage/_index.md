---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words für .NET
description: OleFormat OlePackage eigendom. Zugriff gewähren aufOlePackage wenn das OLEObjekt ein OLEPaket ist. Gibt zurückNull sonst in C#.
type: docs
weight: 80
url: /de/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Zugriff gewähren auf[`OlePackage`](../../olepackage/) wenn das OLE-Objekt ein OLE-Paket ist. Gibt zurück`Null` sonst.

```csharp
public OlePackage OlePackage { get; }
```

## Bemerkungen

OLE Package ist eine Legacy-Technologie, die es ermöglicht, jedes Dateiformat, das nicht in der OLE-Registrierung von einem Windows-System vorhanden ist, in ein generisches Paket zu packen, mit dem fast alles in ein Dokument eingebettet werden kann. Siehe[`OlePackage`](../../olepackage/) Geben Sie für weitere Informationen Folgendes ein.

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
