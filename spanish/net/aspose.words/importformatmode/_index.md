---
title: Enum ImportFormatMode
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.ImportFormatMode enumeración. Especifica cómo se fusiona el formato al importar contenido de otro documento.
type: docs
weight: 3030
url: /es/net/aspose.words/importformatmode/
---
## ImportFormatMode enumeration

Especifica cómo se fusiona el formato al importar contenido de otro documento.

```csharp
public enum ImportFormatMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| UseDestinationStyles | `0` | Usar los estilos del documento de destino y copiar estilos nuevos. Esta es la opción por defecto. |
| KeepSourceFormatting | `1` | Copie todos los estilos requeridos en el documento de destino, genere nombres de estilo únicos si es necesario. |
| KeepDifferentStyles | `2` | Solo copie estilos que sean diferentes a los del documento de origen. |

### Observaciones

Cuando copia nodos de un documento a otro, esta opción especifica cómo se resuelve el formato cuando ambos documentos tienen un estilo con el mismo nombre, pero con un formato diferente.

El formateo se resuelve de la siguiente manera:

1. Los estilos integrados se comparan con su identificador de estilo independiente de la configuración regional. Los estilos definidos por el usuario se comparan con el nombre de estilo que distingue entre mayúsculas y minúsculas.
2. Si no se encuentra un estilo coincidente en el documento de destino, el estilo (y todos los estilos a los que hace referencia) se copian en el documento de destino y los nodos importados se actualizan para hacer referencia al nuevo estilo.
3. Si ya existe un estilo coincidente en el documento de destino, lo que sucede depende del`importFormatMode` parámetro pasado a [`Documento.ImportNode`](../documentbase/importnode/) como se describe a continuación.

Al usar el **Usar estilos de destino**opción, si ya existe un estilo coincidente en el documento de destino, el estilo no se copia y los nodos importados se actualizan para hacer referencia al estilo existente.

El inconveniente de usar **Usar estilos de destino** es que el texto importado podría verse diferente en el documento de destino en comparación con el documento de origen. Por ejemplo, el estilo "Título 1" en el documento de origen usa fuente Arial 16pt y el estilo "Título 1" en el documento de destino usa Times New Fuente Roman 14pt. Al importar texto del estilo "Título 1" sin otro formato directo, aparecerá como fuente Times New Roman 14pt en el documento de destino.

**Coserva el formato original**La opción permite asegurarse de que el contenido importado tenga el mismo aspecto en el documento de destino que en el documento de origen. Si ya existe un estilo coincidente en el documento de destino, el formato del estilo de origen se expande en atributos de nodo directos y el estilo se cambiado a Normal. Si el estilo no existe en el documento de destino, el estilo de origen se importa en el documento de destino y se aplica al nodo importado. Tenga en cuenta que no siempre es posible conservar el estilo de origen incluso si no existe en el documento de destino. En este caso, el formato de dicho estilo se expandirá a los atributos de Nodo directos a favor de preservar el formato de Nodo original.

El inconveniente de usar **Coserva el formato original**es que si realiza varias importaciones, podría terminar con muchos estilos en el documento de destino y eso podría dificultar el uso de formato de estilo coherente en Microsoft Word para este documento.

Usando **MantenerEstilosDiferentes** La opción permite reutilizar los estilos de destino si el formato que proporcionan es idéntico a los estilos del documento de origen. Si el estilo del documento de destino es diferente al del origen, se importa.

### Ejemplos

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


