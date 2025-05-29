---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words para .NET
description: Descubra cómo diseñar la propiedad LinkedStyleName, administrar fácilmente los estilos vinculados y mejorar su flujo de trabajo de diseño con una integración perfecta.
type: docs
weight: 90
url: /es/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

Obtiene/establece el nombre del[`Style`](../) Vinculado a este. Devuelve una cadena vacía si no hay estilos vinculados.

```csharp
public string LinkedStyleName { get; set; }
```

## Observaciones

Sólo se permite vincular el estilo de párrafo al estilo de carácter y viceversa.

La configuración de LinkedStyleName para el estilo actual conduce automáticamente a la configuración de LinkedStyleName para el estilo vinculado.

Asignar la cadena vacía equivale a desvincular el estilo previamente vinculado.

## Ejemplos

Muestra cómo vincular estilos entre sí.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];

Style styleHeading1Char = doc.Styles.Add(StyleType.Character, "Heading 1 Char");
styleHeading1Char.Font.Name = "Verdana";
styleHeading1Char.Font.Bold = true;
styleHeading1Char.Font.Border.LineStyle = LineStyle.Dot;
styleHeading1Char.Font.Border.LineWidth = 15;

styleHeading1.LinkedStyleName = "Heading 1 Char";

Assert.AreEqual("Heading 1 Char", styleHeading1.LinkedStyleName);
Assert.AreEqual("Heading 1", styleHeading1Char.LinkedStyleName);
```

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
