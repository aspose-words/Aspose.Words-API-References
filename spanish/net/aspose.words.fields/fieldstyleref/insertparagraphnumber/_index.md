---
title: FieldStyleRef.InsertParagraphNumber
linktitle: InsertParagraphNumber
articleTitle: InsertParagraphNumber
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldStyleRef InsertParagraphNumber para administrar fácilmente la numeración de párrafos en sus documentos, garantizando referencias precisas y un formato mejorado.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldstyleref/insertparagraphnumber/
---
## FieldStyleRef.InsertParagraphNumber property

Obtiene o establece si se debe insertar el número de párrafo del párrafo referenciado exactamente como aparece en el documento.

```csharp
public bool InsertParagraphNumber { get; set; }
```

## Ejemplos

Muestra cómo utilizar los campos STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree una lista basada en una plantilla de lista de Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

//Esta lista generada mostrará "1.a )".
 // El espacio antes del corchete es un carácter no delimitador, que podemos suprimir.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Agregue texto y aplique estilos de párrafo a los que harán referencia los campos STYLEREF.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Coloque un campo STYLEREF en el encabezado y muestre el primer texto con estilo "Párrafo de lista" en el documento.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Coloque un campo STYLEREF en el pie de página y haga que muestre el último texto.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// También podemos utilizar los campos STYLEREF para hacer referencia a los números de lista de las listas.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Ver también

* class [FieldStyleRef](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
