---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words para .NET
description: La lista de control se fusiona con la propiedad ImportFormatOptions MergePastedLists. Administre fácilmente las listas pegadas para mejorar el formato del documento. El valor predeterminado es falso.
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

Muestra cómo fusionar listas de un documento.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Establezca la propiedad "MergePastedLists" en "true", las listas pegadas se fusionarán con las listas circundantes.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Ver también

* class [ImportFormatOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
