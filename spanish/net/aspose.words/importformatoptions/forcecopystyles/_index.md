---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words para .NET
description: ImportFormatOptions ForceCopyStyles propiedad. Obtiene o establece un valor booleano que indica si se deben copiar estilos conflictivos enKeepSourceFormatting mode. El valor predeterminado esFALSO  en C#.
type: docs
weight: 30
url: /es/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Obtiene o establece un valor booleano que indica si se deben copiar estilos conflictivos enKeepSourceFormatting mode. El valor predeterminado es`FALSO` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## Observaciones

De forma predeterminada, si ya existe un estilo coincidente en un documento de destino, el estilo de origen formatting se expande a atributos de nodo directo y el estilo de este nodo se restablece a su valor predeterminado.

Cuando esta opción está configurada en`verdadero`, el estilo de origen se copiará a la fuerza en el documento de destino con un nombre único y se aplicará al nodo importado.

Tenga en cuenta que en este caso no se garantiza que se conserve el formato del nodo importado en el documento de destino .

## Ejemplos

Muestra cómo copiar a la fuerza estilos de origen con nombres únicos.

```csharp
// Ambos documentos contienen MyStyle1 y MyStyle2, MyStyle3 existe solo en un documento fuente.
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.AreEqual(paras[0].ParagraphFormat.Style.Name, "MyStyle1_0");
Assert.AreEqual(paras[1].ParagraphFormat.Style.Name, "MyStyle2_0");
Assert.AreEqual(paras[2].ParagraphFormat.Style.Name, "MyStyle3");
```

### Ver también

* class [ImportFormatOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
