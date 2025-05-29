---
title: Style.Aliases
linktitle: Aliases
articleTitle: Aliases
second_title: Aspose.Words para .NET
description: Descubra fácilmente todos los alias de estilo con la propiedad Alias de Estilo. Si no existe ninguno, recibirá una matriz de cadenas vacía. ¡Simplifique la gestión de estilos!
type: docs
weight: 10
url: /es/net/aspose.words/style/aliases/
---
## Style.Aliases property

Obtiene todos los alias de este estilo. Si el estilo no tiene alias, se devuelve una matriz de cadenas vacía.

```csharp
public string[] Aliases { get; }
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
