---
title: Frameset.ChildFramesets
second_title: Referencia de API de Aspose.Words para .NET
description: Frameset propiedad. Obtiene la colección de marcos secundarios y páginas de marcos.
type: docs
weight: 20
url: /es/net/aspose.words.framesets/frameset/childframesets/
---
## Frameset.ChildFramesets property

Obtiene la colección de marcos secundarios y páginas de marcos.

```csharp
public FramesetCollection ChildFramesets { get; }
```

### Ejemplos

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

* class [FramesetCollection](../../framesetcollection/)
* class [Frameset](../)
* espacio de nombres [Aspose.Words.Framesets](../../frameset/)
* asamblea [Aspose.Words](../../../)


