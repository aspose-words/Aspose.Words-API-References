---
title: Style.Remove
second_title: Referencia de API de Aspose.Words para .NET
description: Style método. Elimina el estilo especificado del documento.
type: docs
weight: 200
url: /es/net/aspose.words/style/remove/
---
## Style.Remove method

Elimina el estilo especificado del documento.

```csharp
public void Remove()
```

### Observaciones

La eliminación de estilo tiene los siguientes efectos en el modelo del documento:

* Todas las referencias al estilo se eliminan de los párrafos, corridas y tablas correspondientes.
* Si se elimina el estilo base, su formato se mueve a los estilos secundarios.
* Si el estilo que se va a eliminar tiene un estilo vinculado, ambos se eliminarán.

### Ejemplos

Muestra cómo crear y aplicar un estilo personalizado.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Redefinir automáticamente el estilo.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Aplicar uno de los estilos del documento al párrafo que está creando el creador del documento.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Elimina nuestro estilo personalizado de la colección de estilos del documento.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Cualquier texto que utilizó un estilo eliminado vuelve al formato predeterminado.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Ver también

* class [Style](../)
* espacio de nombres [Aspose.Words](../../style/)
* asamblea [Aspose.Words](../../../)


