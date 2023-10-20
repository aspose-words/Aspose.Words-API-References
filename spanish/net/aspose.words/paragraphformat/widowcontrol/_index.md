---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words para .NET
description: ParagraphFormat WidowControl propiedad. Verdadero si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo en C#.
type: docs
weight: 400
url: /es/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Verdadero si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo.

```csharp
public bool WidowControl { get; set; }
```

## Ejemplos

Muestra cómo habilitar el control de viudas/huérfanos para un párrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cuando escribimos texto que no cabe en una página, una línea puede extenderse a la página siguiente.
// La única línea que termina en la página siguiente se llama "Huérfana",
// y la línea anterior donde se interrumpió el huérfano se llama "Viuda".
// Podemos arreglar huérfanos y viudas reorganizando el texto según el tamaño de fuente, el espaciado o los márgenes de la página.
// Si deseamos preservar las dimensiones de nuestro documento, podemos establecer este indicador en "verdadero"
 // para poner a las viudas en la misma página que a sus respectivos huérfanos.
// Dejar esta bandera como "falso" dejará los pares viudo/huérfano en el texto.
// Cada párrafo tiene esta configuración accesible en Microsoft Word a través de Inicio -> Párrafo -> Configuración de párrafo
// (botón en la esquina inferior derecha de la pestaña "Párrafo") -> "Control de viudas y huérfanos".
builder.ParagraphFormat.WidowControl = widowControl; 

// Insertar texto que produzca un huérfano y una viuda.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
