---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words para .NET
description: Descubra el método Range UnlinkFields para desvincular fácilmente campos en su rango de documentos, mejorando su flujo de trabajo y la gestión de documentos.
type: docs
weight: 120
url: /es/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Desvincula campos en este rango.

```csharp
public void UnlinkFields()
```

## Observaciones

Reemplaza todos los campos de este rango con sus resultados más recientes.

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
