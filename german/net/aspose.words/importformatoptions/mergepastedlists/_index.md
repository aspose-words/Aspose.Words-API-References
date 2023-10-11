---
title: ImportFormatOptions.MergePastedLists
second_title: Aspose.Words für .NET-API-Referenz
description: ImportFormatOptions eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt ob eingefügte Listen mit umgebenden Listen zusammengeführt werden. Der Standardwert istFALSCH .
type: docs
weight: 70
url: /de/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden. Der Standardwert ist`FALSCH` .

```csharp
public bool MergePastedLists { get; set; }
```

### Beispiele

Zeigt, wie Listen aus Dokumenten zusammengeführt werden.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Setzen Sie die Eigenschaft „MergePastedLists“ auf „true“, eingefügte Listen werden mit umgebenden Listen zusammengeführt.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Siehe auch

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../importformatoptions/)
* Montage [Aspose.Words](../../../)


