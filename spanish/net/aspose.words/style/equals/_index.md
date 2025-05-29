---
title: Style.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words para .NET
description: Descubra el método "Estilo Igual" para comparar estilos predefinidos. Comprenda los estilos de párrafo enlazado y siguiente para mejorar el formato y la eficiencia del diseño.
type: docs
weight: 220
url: /es/net/aspose.words/style/equals/
---
## Style.Equals method

Se compara con el estilo especificado. Los estilos predeterminados se comparan solo para estilos integrados. Los estilos predeterminados no se incluyen en la comparación. El estilo base, el estilo vinculado y el estilo del siguiente párrafo se comparan de forma recursiva.

```csharp
public bool Equals(Style style)
```

## Ejemplos

Muestra cómo utilizar alias de estilo.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

//Este documento contiene un estilo llamado "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Si el nombre de un estilo tiene varios valores separados por comas, cada cláusula es un alias separado.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

//Podemos referenciar un estilo utilizando su alias, así como su nombre.
Assert.AreEqual(doc.Styles["MyStyle Alias 1"], doc.Styles["MyStyle Alias 2"]);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.AreEqual(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style, 
    doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style);
```

### Ver también

* class [Style](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
