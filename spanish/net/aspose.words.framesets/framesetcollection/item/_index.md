---
title: FramesetCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda a marcos específicos con FramesetCollection. Recupera fácilmente las páginas de marcos por índice para una navegación web eficiente y una experiencia de usuario mejorada.
type: docs
weight: 30
url: /es/net/aspose.words.framesets/framesetcollection/item/
---
## FramesetCollection indexer

Obtiene una página de marco o marcos en el índice especificado.

```csharp
public Frameset this[int index] { get; }
```

## Ejemplos

Muestra cómo acceder a los marcos en la página.

```csharp
//El documento contiene varios marcos con enlaces a otros documentos.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
//Podemos comprobar la URL predeterminada (la URL de una página web o un documento local) o si el marco es un recurso externo.
Assert.AreEqual("https://archivo-ejemplos-com.github.io/uploads/2017/02/archivo-muestra_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Cambiar las propiedades de uno de nuestros marcos.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Ver también

* class [Frameset](../../frameset/)
* class [FramesetCollection](../)
* espacio de nombres [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* asamblea [Aspose.Words](../../../)
