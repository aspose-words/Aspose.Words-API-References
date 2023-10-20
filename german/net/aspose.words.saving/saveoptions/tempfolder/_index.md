---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words für .NET
description: SaveOptions TempFolder eigendom. Gibt den Ordner für temporäre Dateien an die beim Speichern in einer DOC oder DOCXDatei verwendet werden. Standardmäßig ist diese EigenschaftNull und es werden keine temporären Dateien verwendet in C#.
type: docs
weight: 140
url: /de/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Gibt den Ordner für temporäre Dateien an, die beim Speichern in einer DOC- oder DOCX-Datei verwendet werden. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet.

```csharp
public string TempFolder { get; set; }
```

## Bemerkungen

Wenn Aspose.Words ein Dokument speichert, müssen temporäre interne Strukturen erstellt werden. Standardmäßig werden diese internen Strukturen im Speicher erstellt und die Speichernutzung steigt kurzzeitig an, während das Dokument gespeichert wird. Wenn der Speichervorgang abgeschlossen ist, wird der Speicher freigegeben und vom Garbage Collector zurückgefordert.

Wenn Sie ein sehr großes Dokument (Tausende Seiten) speichern und/oder viele Dokumente gleichzeitig verarbeiten, kann die Speicherspitze während des Speicherns so groß sein, dass das System einen Fehler verursachtOutOfMemoryException . Angeben eines temporären Ordners mit`TempFolder` führt dazu, dass Aspose.Words die internen Strukturen in temporären Dateien statt im Speicher behält. Dadurch wird die Speichernutzung beim Speichern reduziert, die Speicherleistung wird jedoch verringert.

Der Ordner muss vorhanden und beschreibbar sein, andernfalls wird eine Ausnahme ausgelöst.

Aspose.Words löscht automatisch alle temporären Dateien, wenn der Speichervorgang abgeschlossen ist.

## Beispiele

Zeigt, wie Sie beim Speichern eines Dokuments die Festplatte anstelle des Speichers verwenden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Wenn wir ein Dokument speichern, werden während des Speichervorgangs verschiedene Elemente vorübergehend im Speicher gespeichert.
// Mit dieser Option können wir stattdessen einen temporären Ordner im lokalen Dateisystem verwenden.
// was den Speicheraufwand unserer Anwendung reduziert.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Der angegebene temporäre Ordner muss vor dem Speichervorgang im lokalen Dateisystem vorhanden sein.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Der Ordner bleibt ohne Restinhalte vom Ladevorgang bestehen.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
