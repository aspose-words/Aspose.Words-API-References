---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words para .NET
description: Descubre si tu página tiene contenido de colores vibrantes con la propiedad PageInfo Colored. ¡Mejora la interacción del usuario y mejora el atractivo visual!
type: docs
weight: 10
url: /es/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Devuelve`verdadero` Si la página contiene contenido en color.

```csharp
public bool Colored { get; }
```

## Ejemplos

Muestra cómo comprobar si la página está en color o no.

```csharp
Document doc = new Document(MyDir + "Document.docx");

//Verifique que la primera página del documento no esté en color.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Ver también

* class [PageInfo](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)
