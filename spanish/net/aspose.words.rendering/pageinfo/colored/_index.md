---
title: PageInfo.Colored
second_title: Referencia de API de Aspose.Words para .NET
description: PageInfo propiedad. Devolucionesverdadero si la página contiene contenido en color.
type: docs
weight: 10
url: /es/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Devoluciones`verdadero` si la página contiene contenido en color.

```csharp
public bool Colored { get; }
```

### Ejemplos

Muestra cómo comprobar si la página está en color o no.

```csharp
Document doc = new Document(MyDir + "Document.docx");

//Comprueba que la primera página del documento no esté coloreada.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Ver también

* class [PageInfo](../)
* espacio de nombres [Aspose.Words.Rendering](../../pageinfo/)
* asamblea [Aspose.Words](../../../)


