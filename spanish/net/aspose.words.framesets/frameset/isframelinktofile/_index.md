---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
articleTitle: IsFrameLinkToFile
second_title: Aspose.Words para .NET
description: Frameset IsFrameLinkToFile propiedad. Obtiene o establece un valor que indica si la página web o el nombre del archivo del documento especificado en FrameDefaultUrl La propiedad es un recurso externo con el que el marco está vinculado en C#.
type: docs
weight: 40
url: /es/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

Obtiene o establece un valor que indica si la página web o el nombre del archivo del documento especificado en [`FrameDefaultUrl`](../framedefaulturl/) La propiedad es un recurso externo con el que el marco está vinculado.

```csharp
public bool IsFrameLinkToFile { get; set; }
```

## Ejemplos

Muestra cómo acceder a los marcos en la página.

```csharp
// El documento contiene varios marcos con enlaces a otros documentos.
Document doc = new Document(MyDir + "Frameset.docx");

// Podemos verificar la URL predeterminada (la URL de una página web o un documento local) o si el marco es un recurso externo.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Cambia las propiedades de uno de nuestros marcos.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Ver también

* class [Frameset](../)
* espacio de nombres [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* asamblea [Aspose.Words](../../../)
