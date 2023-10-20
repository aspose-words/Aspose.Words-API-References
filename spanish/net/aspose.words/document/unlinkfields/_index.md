---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words para .NET
description: Document UnlinkFields método. Desvincula campos en todo el documento en C#.
type: docs
weight: 730
url: /es/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Desvincula campos en todo el documento.

```csharp
public void UnlinkFields()
```

## Observaciones

Reemplaza todos los campos de todo el documento con sus resultados más recientes.

Para desvincular campos en una parte específica del documento utilice[`UnlinkFields`](../../range/unlinkfields/).

## Ejemplos

Muestra cómo desvincular todos los campos del documento.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
