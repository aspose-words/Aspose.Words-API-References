---
title: ParagraphFormat.Style
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Obtiene o establece el estilo de párrafo aplicado a este formato.
type: docs
weight: 330
url: /es/net/aspose.words/paragraphformat/style/
---
## ParagraphFormat.Style property

Obtiene o establece el estilo de párrafo aplicado a este formato.

```csharp
public Style Style { get; set; }
```

### Ejemplos

Muestra cómo crear y utilizar un estilo de párrafo con formato de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un estilo de párrafo personalizado.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Cree una lista y asegúrese de que los párrafos que usan este estilo usen esta lista.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Aplique el estilo de párrafo al párrafo actual del generador de documentos y luego agregue algo de texto.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Cambie el estilo del generador de documentos a uno que no tenga formato de lista y escriba otro párrafo.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Ver también

* class [Style](../../style/)
* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


