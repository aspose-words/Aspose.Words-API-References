---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
articleTitle: IsFrameLinkToFile
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad IsFrameLinkToFile del conjunto de marcos mejora su diseño web al vincular recursos externos sin problemas. ¡Optimice sus marcos para un mejor rendimiento!
type: docs
weight: 40
url: /es/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

Obtiene o establece un valor que indica si el nombre del archivo de documento o página web especificado en [`FrameDefaultUrl`](../framedefaulturl/) La propiedad es un recurso externo con el que está vinculado el marco.

```csharp
public bool IsFrameLinkToFile { get; set; }
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

* class [Frameset](../)
* espacio de nombres [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* asamblea [Aspose.Words](../../../)
