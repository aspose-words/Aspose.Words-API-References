---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words für .NET
description: Optimieren Sie das Lesen von Dokumenten mit der TempFolder-Eigenschaft von LoadOptions. Verwalten Sie temporäre Dateien einfach für eine effiziente Verarbeitung und verbesserte Leistung.
type: docs
weight: 150
url: /de/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Ermöglicht die Verwendung temporärer Dateien beim Lesen von Dokumenten. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet.

```csharp
public string TempFolder { get; set; }
```

## Bemerkungen

Der Ordner muss vorhanden und beschreibbar sein, andernfalls wird eine Ausnahme ausgelöst.

Aspose.Words löscht automatisch alle temporären Dateien, wenn der Lesevorgang abgeschlossen ist.

## Beispiele

Zeigt, wie ein Dokument mithilfe temporärer Dateien geladen wird.

```csharp
// Beachten Sie, dass ein solcher Ansatz den Speicherverbrauch reduzieren kann, aber die Geschwindigkeit beeinträchtigt
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Sicherstellen, dass das Verzeichnis existiert und laden
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Zeigt, wie beim Laden eines Dokuments die Festplatte anstelle des Speichers verwendet wird.

```csharp
// Wenn wir ein Dokument laden, werden während des Speichervorgangs verschiedene Elemente vorübergehend im Speicher abgelegt.
// Wir können diese Option verwenden, um stattdessen einen temporären Ordner im lokalen Dateisystem zu verwenden.
// wodurch der Speicheraufwand unserer Anwendung reduziert wird.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Der angegebene temporäre Ordner muss vor dem Ladevorgang im lokalen Dateisystem vorhanden sein.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Der Ordner bleibt bestehen und enthält keinen Restinhalt vom Ladevorgang.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
