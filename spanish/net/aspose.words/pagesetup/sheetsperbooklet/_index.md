---
title: PageSetup.SheetsPerBooklet
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Devuelve o establece el número de páginas que se incluirán en cada folleto.
type: docs
weight: 390
url: /es/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Devuelve o establece el número de páginas que se incluirán en cada folleto.

```csharp
public int SheetsPerBooklet { get; set; }
```

### Ejemplos

Muestra cómo configurar un documento que se puede imprimir como un pliegue de libro.

```csharp
Document doc = new Document();

// Insertar texto que abarque 16 páginas.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de un pliegue de libro.
// Cuando imprimimos este documento por ambos lados, podemos tomar las páginas para apilarlas
// y doblarlos todos por la mitad a la vez. El contenido del documento se alineará en un pliegue de libro.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Solo podemos especificar el número de hojas en múltiplos de 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


