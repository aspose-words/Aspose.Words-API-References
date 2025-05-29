---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words para .NET
description: Descubra la propiedad ForceCopyStyles de ImportFormatOptions, que permite controlar fácilmente la copia de estilos en el modo KeepSourceFormatting. El valor predeterminado es "false" para obtener resultados óptimos.
type: docs
weight: 30
url: /es/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Obtiene o establece un valor booleano que indica que se deben copiar los estilos conflictivos enKeepSourceFormatting mode. El valor predeterminado es`FALSO` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## Observaciones

De forma predeterminada, si ya existe un estilo coincidente en un documento de destino, el estilo de origen formatting se expande en atributos de nodo directo y el estilo de este nodo se restablece a un valor predeterminado.

Cuando esta opción está configurada en`verdadero`, el estilo de origen se copiará forzosamente en el documento de destino con un nombre único y se aplicará al nodo importado.

Tenga en cuenta que, en este caso, no se garantiza que se conserve el formato del nodo importado en el documento de destino document .

## Ejemplos

Muestra cómo copiar estilos de origen con nombres únicos de manera forzada.

```csharp
// Ambos documentos contienen MyStyle1 y MyStyle2, MyStyle3 solo existe en un documento fuente.
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
