---
title: Style.Equals
second_title: Referencia de API de Aspose.Words para .NET
description: Style método. Compara con el estilo especificado. Las listas de estilos se comparan solo para los estilos integrados. Los estilos predeterminados no se incluyen en la comparación. El estilo base el estilo vinculado y el estilo del siguiente párrafo se comparan recursivamente.
type: docs
weight: 170
url: /es/net/aspose.words/style/equals/
---
## Style.Equals method

Compara con el estilo especificado. Las listas de estilos se comparan solo para los estilos integrados. Los estilos predeterminados no se incluyen en la comparación. El estilo base, el estilo vinculado y el estilo del siguiente párrafo se comparan recursivamente.

```csharp
public bool Equals(Style style)
```

### Ejemplos

Muestra cómo usar alias de estilo.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Este documento contiene un estilo llamado "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Si el nombre de un estilo tiene varios valores separados por comas, cada cláusula es un alias independiente.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Podemos hacer referencia a un estilo utilizando su alias, así como su nombre.
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
* espacio de nombres [Aspose.Words](../../style/)
* asamblea [Aspose.Words](../../../)


