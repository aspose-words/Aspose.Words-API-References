---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: Aspose.Words para .NET
description: Aspose.Words.ImportFormatMode enumeración. Especifica cómo se combina el formato al importar contenido de otro documento en C#.
type: docs
weight: 3230
url: /es/net/aspose.words/importformatmode/
---
## ImportFormatMode enumeration

Especifica cómo se combina el formato al importar contenido de otro documento.

```csharp
public enum ImportFormatMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| UseDestinationStyles | `0` | Utilice los estilos del documento de destino y copie nuevos estilos. Esta es la opción predeterminada. |
| KeepSourceFormatting | `1` | Copie todos los estilos requeridos en el documento de destino, genere nombres de estilo únicos si es necesario. |
| KeepDifferentStyles | `2` | Copie únicamente estilos que sean diferentes a los del documento fuente. |

## Observaciones

Cuando copia nodos de un documento a otro, esta opción especifica cómo se resuelve formatting cuando ambos documentos tienen un estilo con el mismo nombre, pero con diferente formato.

El formateo se resuelve de la siguiente manera:

1. Los estilos integrados se combinan utilizando su identificador de estilo independiente de la configuración regional. Los estilos definidos por el usuario se combinan utilizando un nombre de estilo que distingue entre mayúsculas y minúsculas.
2. Si no se encuentra un estilo coincidente en el documento de destino, style (y todos los estilos a los que hace referencia) se copian en el documento de destino y los nodos importados se actualizan para hacer referencia al nuevo estilo.
3. Si ya existe un estilo coincidente en el documento de destino, lo que sucede depende del`importar modo formato` parámetro pasado a [`Documento.ImportNode`](../documentbase/importnode/) como se describe a continuación.

Al usar elUseDestinationStyles Opción, si ya existe un estilo coincidente en el documento de destino, el estilo no se copia y los nodos importados se actualizan para hacer referencia al estilo existente.

El inconveniente de utilizarUseDestinationStyleses que el texto importado podría verse diferente en el documento de destino en comparación con el documento de origen. Por ejemplo, el estilo "Título 1" en el documento de origen usa fuente Arial de 16 puntos y el estilo "Título 1" en el documento de destino usa Times New Fuente Roman de 14 puntos. Al importar texto de estilo "Título 1" sin ningún otro formato directo, aparecerá como fuente Times New Roman de 14 puntos en el documento de destino.

KeepSourceFormattingLa opción permite asegurarse de que el contenido importado tenga el mismo aspecto en el documento de destino que en el documento de origen. Si ya existe un estilo coincidente en el documento de destino, el formato del estilo de origen se expande en atributos directos de Nodo y el estilo es cambiado a Normal. Si el estilo no existe en el documento de destino, entonces el estilo de origen se importa en el documento de destino y se aplica al nodo importado. Tenga en cuenta que no siempre es posible conservar el estilo de origen incluso si no existe en el documento de destino. En este caso, el formato de dicho estilo se expandirá a atributos directos del Nodo para preservar el formato original del Nodo.

El inconveniente de utilizarKeepSourceFormattinges que si realiza varias importaciones, podría terminar con muchos estilos en el documento de destino y eso podría dificultar el uso de un formato de estilo consistente en Microsoft Word para este documento.

UsandoKeepDifferentStyles La opción permite reutilizar los estilos de destino si el formato que proporcionan es idéntico a los estilos en el documento de origen. Si el estilo en el documento de destino es diferente al de origen, entonces se importa.

## Ejemplos

Muestra cómo insertar un documento en otro documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
