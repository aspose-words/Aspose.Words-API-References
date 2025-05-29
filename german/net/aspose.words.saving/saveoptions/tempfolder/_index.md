---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words für .NET
description: Optimieren Sie das Speichern Ihrer Dokumente mit der SaveOptions TempFolder-Eigenschaft, die einen Ordner für temporäre DOC- und DOCX-Dateien festlegt und so die Effizienz steigert.
type: docs
weight: 140
url: /de/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet.

```csharp
public string TempFolder { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| OutOfMemoryException | Wird ausgelöst, wenn Sie ein sehr großes Dokument (Tausende von Seiten) speichern und/oder viele Dokumente gleichzeitig verarbeiten. Die Speicherspitze während des Speicherns kann groß genug sein, um die Ausnahme zu verursachen. |

## Bemerkungen

Wenn Aspose.Words ein Dokument speichert, müssen temporäre interne Strukturen erstellt werden. Standardmäßig werden diese internen Strukturen im Speicher erstellt, und die Speicherauslastung steigt während des Speicherns des Dokuments kurzzeitig an. Nach Abschluss des Speichervorgangs wird der Speicher freigegeben und vom Garbage Collector freigegeben.

Festlegen eines temporären Ordners mit`TempFolder` bewirkt, dass Aspose.Words die internen Strukturen in temporären Dateien (x000d) statt im Speicher speichert. Dies reduziert den Speicherverbrauch beim Speichern, verringert jedoch die Speicherleistung.

Der Ordner muss vorhanden und beschreibbar sein, andernfalls wird eine Ausnahme ausgelöst.

Aspose.Words löscht nach Abschluss des Speichervorgangs automatisch alle temporären Dateien.

## Beispiele

Zeigt, wie beim Speichern eines Dokuments die Festplatte anstelle des Arbeitsspeichers verwendet wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Wenn wir ein Dokument speichern, werden während des Speichervorgangs verschiedene Elemente vorübergehend im Speicher abgelegt.
// Wir können diese Option verwenden, um stattdessen einen temporären Ordner im lokalen Dateisystem zu verwenden.
// wodurch der Speicheraufwand unserer Anwendung reduziert wird.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Der angegebene temporäre Ordner muss vor dem Speichervorgang im lokalen Dateisystem vorhanden sein.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Der Ordner bleibt bestehen und enthält keinen Restinhalt vom Ladevorgang.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
