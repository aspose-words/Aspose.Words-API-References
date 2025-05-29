---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar el método UnlinkFields para desvincular campos de manera eficiente en todo su documento, mejorando su flujo de trabajo de edición.
type: docs
weight: 780
url: /es/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Desvincula campos en todo el documento.

```csharp
public void UnlinkFields()
```

## Observaciones

Reemplaza todos los campos del documento completo con sus resultados más recientes.

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
