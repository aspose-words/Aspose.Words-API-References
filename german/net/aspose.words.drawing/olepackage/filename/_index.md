---
title: OlePackage.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words für .NET
description: Entdecken Sie die OlePackage FileName-Eigenschaft zur einfachen Verwaltung von OLE-Paketdateinamen. Verbessern Sie Ihre Datenverarbeitung durch nahtlose Integration und Flexibilität.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/olepackage/filename/
---
## OlePackage.FileName property

Ruft den Dateinamen des OLE-Pakets ab oder legt ihn fest.

```csharp
public string FileName { get; set; }
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
