---
title: OlePackage
second_title: Aspose.Words für .NET-API-Referenz
description: Zugriff gewähren aufOlePackageaspose.words.drawing/olepackage wenn OLE-Objekt ein OLE-Paket ist. Gibt ansonsten null zurück.
type: docs
weight: 80
url: /de/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Zugriff gewähren auf[`OlePackage`](../../olepackage) wenn OLE-Objekt ein OLE-Paket ist. Gibt ansonsten null zurück.

```csharp
public OlePackage OlePackage { get; }
```

### Bemerkungen

Das OLE-Paket ist eine Legacy-Technologie, die es ermöglicht, jedes Dateiformat, das nicht in der OLE-Registrierung eines Windows-Systems vorhanden ist, in ein generisches Paket zu packen, das es ermöglicht, fast alles in ein Dokument einzubetten. Siehe[`OlePackage`](../../olepackage)Geben Sie für weitere Informationen ein.

### Beispiele

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

* class [OlePackage](../../olepackage)
* class [OleFormat](../../oleformat)
* namensraum [Aspose.Words.Drawing](../../oleformat)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->