---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words para .NET
description: Descubra la propiedad NavigationMapLevel de HtmlSaveOptions, que controla los niveles de encabezado en las exportaciones EPUB, MOBI y AZW3. ¡Maximice la visibilidad de su contenido!
type: docs
weight: 390
url: /es/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Especifica el nivel máximo de encabezados que se pueden rellenar en el mapa de navegación al exportar a los formatos EPUB, MOBI o AZW3 . El valor predeterminado es`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Observaciones

El mapa de navegación permite a los agentes de usuario facilitar la navegación por la estructura del documento. Normalmente, los puntos de navegación corresponden a los encabezados del documento. Para completar los encabezados hasta el nivel**norte** asigna este valor a`NavigationMapLevel`.

De forma predeterminada, se completan tres niveles de encabezados: párrafos de estilos**Título 1** ,**Título 2** y**Título 3**. Puede establecer esta propiedad en un valor de 1 a 9 para solicitar el nivel máximo correspondiente. Establecerla en cero reducirá el mapa de navegación solo a la raíz del documento o a las raíces de las partes del documento.

## Ejemplos

Muestra cómo generar una tabla de contenido para documentos Azw3.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Azw3);
options.NavigationMapLevel = 2;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

Muestra cómo generar una tabla de contenidos para documentos Mobi.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mobi);
options.NavigationMapLevel = 5;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

Muestra cómo filtrar los encabezados que aparecen en el panel de navegación de un documento Epub guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//Cada párrafo que formateamos utilizando un estilo "Encabezado" puede servir como encabezado.
// Cada encabezado también puede tener un nivel de encabezado, determinado por el número de su estilo de encabezado.
//Los títulos a continuación son de los niveles 1-3.
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

// Los lectores de Epub normalmente crean una tabla de contenidos para sus documentos.
// Cada párrafo con un estilo "Encabezado" en el documento creará una entrada en esta tabla de contenidos.
 //Podemos utilizar la propiedad "NavigationMapLevel" para establecer un nivel de rumbo máximo.
//El lector de Epub no agregará encabezados con un nivel superior al que especifiquemos a la tabla de contenidos.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.NavigationMapLevel = 2;

//Nuestro documento tiene seis encabezados, dos de los cuales están por encima del nivel 2.
//La tabla de contenidos de este documento tendrá cuatro entradas.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
