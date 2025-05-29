---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words für .NET
description: Steuern Sie die Listenzusammenführung mit der Eigenschaft „MergePastedLists“ von ImportFormatOptions. Verwalten Sie eingefügte Listen einfach, um die Dokumentformatierung zu verbessern. Standardwert: „false“.
type: docs
weight: 70
url: /de/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden. Der Standardwert ist`FALSCH` .

```csharp
public bool MergePastedLists { get; set; }
```

## Beispiele

Zeigt, wie Listen aus einem Dokument zusammengeführt werden.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Setzen Sie die Eigenschaft „MergePastedLists“ auf „true“. Eingefügte Listen werden mit umgebenden Listen zusammengeführt.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Siehe auch

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
