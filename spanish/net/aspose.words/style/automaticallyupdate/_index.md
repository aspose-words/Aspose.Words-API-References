---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad AutomaticallyUpdate mejora sus estilos al redefinirlos automáticamente para obtener un valor y rendimiento óptimos en sus proyectos.
type: docs
weight: 20
url: /es/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Especifica si este estilo se redefine automáticamente en función del valor apropiado.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## Observaciones

Si el valor de la propiedad se establece como verdadero, MS Word redefine automáticamente el estilo actual cuando se cambia el formato de párrafo apropiado.

La propiedad AutomaticallyUpdate se aplica únicamente a los estilos de párrafo.

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo crear y aplicar un estilo personalizado.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Redefinir el estilo automáticamente.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Aplicar uno de los estilos del documento al párrafo que está creando el generador de documentos.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

//Elimina nuestro estilo personalizado de la colección de estilos del documento.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Cualquier texto que utilice un estilo eliminado vuelve al formato predeterminado.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Ver también

* class [Style](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
