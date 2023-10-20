---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words para .NET
description: ImportFormatOptions MergePastedLists propiedad. Obtiene o establece un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes. El valor predeterminado esFALSO  en C#.
type: docs
weight: 70
url: /es/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Obtiene o establece un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes. El valor predeterminado es`FALSO` .

```csharp
public bool MergePastedLists { get; set; }
```

## Ejemplos

Muestra cómo fusionar listas de documentos.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Establece la propiedad "MergePastedLists" en "verdadero". Las listas pegadas se fusionarán con las listas circundantes.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Ver también

* class [ImportFormatOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
