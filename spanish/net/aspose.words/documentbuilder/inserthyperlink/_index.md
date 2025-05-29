---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words para .NET
description: Mejore sus documentos con el método InsertHyperlink de DocumentBuilder, agregando sin esfuerzo enlaces en los que se puede hacer clic para mejorar la navegación y la participación del usuario.
type: docs
weight: 390
url: /es/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Inserta un hipervínculo en el documento.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| displayText | String | Texto del enlace que se mostrará en el documento. |
| urlOrBookmark | String | Destino del enlace. Puede ser una URL o el nombre de un marcador dentro del documento. Este método siempre añade apóstrofes al principio y al final de la URL. |
| isBookmark | Boolean | `verdadero` si el parámetro anterior es un nombre de un marcador dentro del documento; `FALSO` El parámetro anterior es una URL. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo insertado.

## Observaciones

Tenga en cuenta que debe especificar el formato de fuente para el texto que se muestra en el hipervínculo explícitamente utilizando el[`Font`](../font/) propiedad.

Este método llama internamente[`InsertField`](../insertfield/)para insertar un campo HIPERVÍNCULO de MS Word en el documento.

## Ejemplos

Muestra cómo insertar un campo de hipervínculo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Inserta un hipervínculo y enfatízalo con formato personalizado.
// El hipervínculo será un fragmento de texto en el que se puede hacer clic y que nos llevará a la ubicación especificada en la URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falso);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic izquierdo en el enlace del texto en Microsoft Word nos llevará a la URL a través de una nueva ventana del navegador web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Muestra cómo insertar un hipervínculo que hace referencia a un marcador local.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Insertar un campo HIPERVÍNCULO que enlaza al marcador. Podemos pasar modificadores de campo.
// al método "InsertHyperlink" como parte del argumento que contiene el nombre del marcador referenciado.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Muestra cómo utilizar la pila de formato de un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configure el formato de fuente y luego escriba el texto que va antes del hipervínculo.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Conservamos nuestra configuración de formato actual en la pila.
builder.PushFont();

// Modifique el formato actual del constructor aplicando un nuevo estilo.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", falso);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Restaura el formato de fuente que guardamos anteriormente y elimina el elemento de la pila.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
