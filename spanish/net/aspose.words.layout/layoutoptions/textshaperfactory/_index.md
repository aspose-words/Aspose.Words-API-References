---
title: LayoutOptions.TextShaperFactory
second_title: Referencia de API de Aspose.Words para .NET
description: LayoutOptions propiedad. Obtiene o estableceITextShaperFactory implementación utilizada para funciones de representación de tipografía avanzada.
type: docs
weight: 100
url: /es/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Obtiene o establece[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) implementación utilizada para funciones de representación de tipografía avanzada.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

### Ejemplos

Muestra cómo admitir funciones OpenType utilizando el motor de modelado de texto HarfBuzz.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words puede usar objetos formadores de texto proporcionados externamente,
// que representan fuentes y calculan información de forma para el texto.
// Es necesaria una fábrica de modeladores de texto para documentos que utilizan varias fuentes.
// Cuando el modelador de texto está configurado de fábrica, el diseño utiliza funciones OpenType.
// Una propiedad de instancia devuelve un objeto estático BasicTextShaperCache que envuelve HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// Actualmente, la configuración del texto se realiza al exportar a formatos PDF o XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Ver también

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../layoutoptions/)
* asamblea [Aspose.Words](../../../)


