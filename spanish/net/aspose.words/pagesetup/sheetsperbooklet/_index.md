---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words para .NET
description: Descubra la propiedad PageSetup SheetsPerBooklet para administrar fácilmente el número de páginas del folleto, mejorando el diseño de su documento y la eficiencia de impresión.
type: docs
weight: 400
url: /es/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Devuelve o establece el número de páginas que se incluirán en cada folleto.

```csharp
public int SheetsPerBooklet { get; set; }
```

## Ejemplos

Muestra cómo configurar un documento que se puede imprimir como un libro plegable.

```csharp
Document doc = new Document();

// Insertar texto que abarca 16 páginas.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de libro plegable.
// Cuando imprimimos este documento por ambas caras, podemos tomar las páginas para apilarlas
// y dóblalos todos por la mitad a la vez. El contenido del documento se alineará formando un pliegue.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

//Solo podemos especificar el número de hojas en múltiplos de 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
