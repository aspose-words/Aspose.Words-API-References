---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words para .NET
description: Descubra el método CompositeNode GetText para recuperar texto de manera eficiente de los nodos y sus hijos, mejorando sus capacidades de procesamiento de datos.
type: docs
weight: 130
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

// GetText recuperará el texto visible, así como los códigos de campo y caracteres especiales.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString nos dará la apariencia del documento si se guarda en un formato de guardado aprobado.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
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

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Ver también

* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
