---
title: HtmlSaveOptions.EpubNavigationMapLevel
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Especifica el nivel máximo de encabezados que se completan en el mapa de navegación cuando se exporta a formato IDPF EPUB. El valor predeterminado es3 .
type: docs
weight: 110
url: /es/net/aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/
---
## HtmlSaveOptions.EpubNavigationMapLevel property

Especifica el nivel máximo de encabezados que se completan en el mapa de navegación cuando se exporta a formato IDPF EPUB. El valor predeterminado es`3` .

```csharp
public int EpubNavigationMapLevel { get; set; }
```

### Observaciones

El mapa de navegación en formato IDPF EPUB permite que los agentes de usuario proporcionen una manera fácil de navegar a través de la estructura del documento. Por lo general, los puntos de navegación corresponden a encabezados en el documento. Para completar encabezados hasta el nivel **norte** asignar este valor a`EpubNavigationMapLevel`.

De forma predeterminada, se rellenan tres niveles de encabezados: párrafos de estilos **Título 1** , **Título 2** y **Título 3**. Puede establecer esta propiedad en un valor de 1 a 9 para solicitar el nivel máximo correspondiente. Establecerlo en cero reducirá el mapa de navegación a solo la raíz del documento o las raíces de las partes del documento.

### Ejemplos

Muestra cómo filtrar los encabezados que aparecen en el panel de navegación de un documento Epub guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cada párrafo al que formateamos usando un estilo "Encabezado" puede servir como encabezado.
// Cada encabezado también puede tener un nivel de encabezado, determinado por el número de su estilo de encabezado.
// Los encabezados a continuación son de los niveles 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Los lectores de Epub normalmente crean una tabla de contenido para sus documentos.
// Cada párrafo con un estilo de "Título" en el documento creará una entrada en esta tabla de contenido.
  // Podemos usar la propiedad "EpubNavigationMapLevel" para establecer un nivel de encabezado máximo.
// El lector de Epub no agregará encabezados con un nivel superior al que especificamos en la tabla de contenidos.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.EpubNavigationMapLevel = 2;

// Nuestro documento tiene seis encabezados, dos de los cuales están por encima del nivel 2.
// La tabla de contenido de este documento tendrá cuatro entradas.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


