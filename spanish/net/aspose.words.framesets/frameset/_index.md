---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words para .NET
description: Descubre la clase Aspose.Words.Framesets.Frameset para una gestión fluida de marcos en documentos. ¡Mejora tus páginas web con una eficiente integración de marcos!
type: docs
weight: 3510
url: /es/net/aspose.words.framesets/frameset/
---
## Frameset class

Representa una página de marcos o un solo marco en una página de marcos.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) Artículo de documentación.

```csharp
public class Frameset
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Frameset](frameset/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | Obtiene la colección de marcos secundarios y páginas de marcos. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Obtiene o establece la URL de la página web o el nombre del archivo del documento que se mostrará en este marco. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Obtiene o establece un valor que indica si el nombre del archivo de documento o página web especificado en [`FrameDefaultUrl`](./framedefaulturl/) La propiedad es un recurso externo con el que está vinculado el marco. |

## Observaciones

Si el[`ChildFramesets`](./childframesets/) La propiedad contiene elementos, esta instancia es una página de marcos, de lo contrario es un solo marco.

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

* espacio de nombres [Aspose.Words.Framesets](../../aspose.words.framesets/)
* asamblea [Aspose.Words](../../)
