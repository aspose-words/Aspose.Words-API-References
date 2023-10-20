---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words para .NET
description: Range UnlinkFields método. Desvincula campos en este rango en C#.
type: docs
weight: 110
url: /es/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Desvincula campos en este rango.

```csharp
public void UnlinkFields()
```

## Observaciones

Reemplaza todos los campos en este rango con sus resultados más recientes.

Para desvincular campos en todo el documento utilice`UnlinkFields`.

## Ejemplos

Muestra cómo desvincular todos los campos de un rango.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### Ver también

* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
