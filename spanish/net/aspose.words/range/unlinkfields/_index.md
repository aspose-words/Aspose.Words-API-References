---
title: Range.UnlinkFields
second_title: Referencia de API de Aspose.Words para .NET
description: Range método. Desvincula campos en este rango.
type: docs
weight: 100
url: /es/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Desvincula campos en este rango.

```csharp
public void UnlinkFields()
```

### Observaciones

Reemplaza todos los campos en este rango con sus resultados más recientes.

Para desvincular campos en todo el documento, use`UnlinkFields`.

### Ejemplos

Muestra cómo desvincular todos los campos de un rango.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### Ver también

* class [Range](../)
* espacio de nombres [Aspose.Words](../../range/)
* asamblea [Aspose.Words](../../../)


