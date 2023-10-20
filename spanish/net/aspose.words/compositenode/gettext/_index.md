---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words para .NET
description: CompositeNode GetText método. Obtiene el texto de este nodo y de todos sus hijos en C#.
type: docs
weight: 110
url: /es/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Obtiene el texto de este nodo y de todos sus hijos.

```csharp
public override string GetText()
```

## Observaciones

La cadena devuelta incluye todos los caracteres de control y especiales como se describe en[`ControlChar`](../../controlchar/).

## Ejemplos

Muestra la diferencia entre llamar a los métodos GetText y ToString en un nodo.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText recuperará el texto visible así como códigos de campo y caracteres especiales.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString nos dará la apariencia del documento si se guarda en un formato de guardado aprobado.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Muestra cómo generar todos los párrafos de un documento que son elementos de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Ver también

* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
