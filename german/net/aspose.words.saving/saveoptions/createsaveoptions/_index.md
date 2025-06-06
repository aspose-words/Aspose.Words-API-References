---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
articleTitle: CreateSaveOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode CreateSaveOptions, um ganz einfach Speicheroptionen zu generieren, die auf Ihr bevorzugtes Format zugeschnitten sind, und so die Effizienz Ihrer Dokumentenverwaltung zu steigern.
type: docs
weight: 10
url: /de/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#createsaveoptions}

Erstellt ein Speicheroptionsobjekt einer Klasse, die für das angegebene Speicherformat geeignet ist.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | SaveFormat | Das Speicherformat, für das ein Speicheroptionsobjekt erstellt werden soll. |

### Rückgabewert

Ein Objekt einer Klasse, die abgeleitet ist von[`SaveOptions`](../).

## Beispiele

Zeigt eine Option zur Optimierung des Speicherverbrauchs beim Rendern großer Dokumente in PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Setzen Sie die Eigenschaft „MemoryOptimization“ auf „true“, um den Speicherbedarf beim Speichern großer Dokumente zu verringern
// auf Kosten einer Verlängerung der Operationsdauer.
// Setzen Sie die Eigenschaft „MemoryOptimization“ auf „false“, um das Dokument normal als PDF zu speichern.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)

---

## CreateSaveOptions(*string*) {#createsaveoptions_1}

Erstellt ein Speicheroptionsobjekt einer Klasse, die für die im angegebenen Dateinamen angegebene Dateierweiterung geeignet ist.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Die Erweiterung dieses Dateinamens bestimmt die Klasse des zu erstellenden Speicheroptionenobjekts. |

### Rückgabewert

Ein Objekt einer Klasse, die abgeleitet ist von[`SaveOptions`](../).

## Beispiele

Zeigt, wie eine Standardvorlage für Dokumente festgelegt wird, denen keine Vorlagen angehängt sind.

```csharp
Document doc = new Document();

// Automatische Stilaktualisierung aktivieren, aber kein Vorlagendokument anhängen.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Da es kein Vorlagendokument gibt, gab es im Dokument keine Möglichkeit, Stiländerungen nachzuverfolgen.
// Verwenden Sie ein SaveOptions-Objekt, um automatisch eine Vorlage festzulegen
// wenn ein Dokument, das wir speichern, keines hat.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
