---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ParagraphFormat WidowControl garantiza que la primera y la última línea de su texto permanezcan juntas en la misma página para una mejor legibilidad.
type: docs
weight: 410
url: /es/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Verdadero si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo.

```csharp
public bool WidowControl { get; set; }
```

## Ejemplos

Muestra cómo habilitar el control de viudas/huérfanas para un párrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cuando escribimos un texto que no cabe en una página, una línea puede extenderse a la página siguiente.
// La línea única que termina en la página siguiente se llama "Huérfana",
// y la línea anterior donde se interrumpió el huérfano se llama "Viuda".
// Podemos corregir textos huérfanos y viudos reorganizando el texto mediante el tamaño de fuente, el espaciado o los márgenes de página.
// Si deseamos preservar las dimensiones de nuestro documento, podemos establecer este indicador en "verdadero"
// para poner a las viudas en la misma página que sus respectivos huérfanos.
// Dejar esta bandera como "falso" dejará pares viudos/huérfanos en el texto.
// Cada párrafo tiene esta configuración accesible en Microsoft Word a través de Inicio -> Párrafo -> Configuración de párrafo
// (botón en la esquina inferior derecha de la pestaña "Párrafo") -> "Control de viudas/huérfanos".
builder.ParagraphFormat.WidowControl = widowControl; 

// Insertar texto que produce un huérfano y una viuda.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
