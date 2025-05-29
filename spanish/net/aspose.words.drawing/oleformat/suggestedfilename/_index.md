---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: Aspose.Words para .NET
description: Descubra la propiedad OleFormat SuggestedFileName para recuperar fácilmente el nombre de archivo recomendado para guardar sus objetos incrustados sin problemas.
type: docs
weight: 130
url: /es/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Obtiene el nombre de archivo sugerido para el objeto incrustado actual si desea guardarlo en un archivo.

```csharp
public string SuggestedFileName { get; }
```

## Ejemplos

Muestra cómo obtener el nombre de archivo sugerido de un objeto OLE.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape)doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// Los objetos OLE pueden proporcionar un nombre de archivo y una extensión sugeridos,
// que podemos usar al guardar el contenido del objeto en un archivo en el sistema de archivos local.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### Ver también

* class [OleFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
