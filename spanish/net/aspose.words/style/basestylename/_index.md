---
title: Style.BaseStyleName
linktitle: BaseStyleName
articleTitle: BaseStyleName
second_title: Aspose.Words para .NET
description: Descubre cómo personalizar la propiedad BaseStyleName para mejorar tu diseño. ¡Obtén o establece fácilmente el nombre del estilo para un aspecto visual más atractivo!
type: docs
weight: 30
url: /es/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

Obtiene/establece el nombre del estilo en el que se basa este estilo.

```csharp
public string BaseStyleName { get; set; }
```

## Observaciones

Esta será una cadena vacía si el estilo no se basa en ningún otro estilo y se puede establecer como una cadena vacía.

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
