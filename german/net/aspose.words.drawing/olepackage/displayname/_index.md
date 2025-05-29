---
title: OlePackage.DisplayName
linktitle: DisplayName
articleTitle: DisplayName
second_title: Aspose.Words für .NET
description: Entdecken Sie die OlePackage DisplayName-Eigenschaft zur einfachen Verwaltung von OLE-Paket-Anzeigenamen. Verbessern Sie Ihre Datenorganisation mit dieser wichtigen Funktion.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/olepackage/displayname/
---
## OlePackage.DisplayName property

Ruft den Anzeigenamen des OLE-Pakets ab oder legt ihn fest.

```csharp
public string DisplayName { get; set; }
```

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

* class [OlePackage](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
