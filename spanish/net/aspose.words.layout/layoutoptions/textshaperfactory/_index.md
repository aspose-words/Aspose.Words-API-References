---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words para .NET
description: Descubra la propiedad LayoutOptions TextShaperFactory para tipografía avanzada. Mejore su renderizado con implementaciones personalizables de ITextShaperFactory.
type: docs
weight: 100
url: /es/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Obtiene o establece[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) Implementación utilizada para funciones de representación de tipografía avanzada.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## Ejemplos

Muestra cómo admitir funciones OpenType mediante el motor de modelado de texto HarfBuzz.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words puede usar objetos modeladores de texto proporcionados externamente,
// que representan fuentes y calculan información de forma para el texto.
// Una fábrica de modeladores de texto es necesaria para documentos que utilizan múltiples fuentes.
// Cuando se configura la fábrica del modelador de texto, el diseño utiliza funciones OpenType.
// Una propiedad de instancia devuelve un objeto BasicTextShaperCache estático que envuelve HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

//Actualmente, la modelación del texto se realiza al exportar a formatos PDF o XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Ver también

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
