---
title: LoadOptions.TempFolder
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions eigendom. Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. Standardmäßig ist diese EigenschaftNull und es werden keine temporären Dateien verwendet.
type: docs
weight: 150
url: /de/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet.

```csharp
public string TempFolder { get; set; }
```

### Bemerkungen

Der Ordner muss vorhanden und beschreibbar sein, andernfalls wird eine Ausnahme ausgelöst.

Aspose.Words löscht automatisch alle temporären Dateien, wenn das Lesen abgeschlossen ist.

### Beispiele

Zeigt, wie ein Dokument mit temporären Dateien geladen wird.

```csharp
// Beachten Sie, dass ein solcher Ansatz die Speichernutzung reduzieren kann, aber die Geschwindigkeit verringert
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Sicherstellen, dass das Verzeichnis existiert und laden
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Zeigt, wie beim Laden eines Dokuments die Festplatte anstelle des Arbeitsspeichers verwendet wird.

```csharp
// Wenn wir ein Dokument laden, werden während des Speichervorgangs verschiedene Elemente vorübergehend im Speicher gespeichert.
// Wir können diese Option verwenden, um stattdessen einen temporären Ordner im lokalen Dateisystem zu verwenden,
// was den Speicheraufwand unserer Anwendung reduziert.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Der angegebene temporäre Ordner muss vor dem Ladevorgang im lokalen Dateisystem vorhanden sein.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Der Ordner wird ohne Restinhalte aus dem Ladevorgang bestehen bleiben.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


