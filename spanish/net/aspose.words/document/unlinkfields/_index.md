---
title: Document.UnlinkFields
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Desvincula campos de todo el documento.
type: docs
weight: 710
url: /es/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Desvincula campos de todo el documento.

```csharp
public void UnlinkFields()
```

### Observaciones

Reemplaza todos los campos en todo el documento con sus resultados más recientes.

Para desvincular campos en una parte específica del documento, use[`UnlinkFields`](../../range/unlinkfields/).

### Ejemplos

Muestra cómo desvincular todos los campos del documento.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


