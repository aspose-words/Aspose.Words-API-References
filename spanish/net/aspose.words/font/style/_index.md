---
title: Font.Style
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Obtiene o establece el estilo de carácter aplicado a este formato.
type: docs
weight: 400
url: /es/net/aspose.words/font/style/
---
## Font.Style property

Obtiene o establece el estilo de carácter aplicado a este formato.

```csharp
public Style Style { get; set; }
```

### Ejemplos

Aplica un subrayado doble a todas las ejecuciones de un documento formateadas con estilos de caracteres personalizados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta un estilo personalizado y aplícalo al texto creado con un generador de documentos.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Iterar sobre cada ejecución y agregar un doble subrayado a cada estilo personalizado.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    Style charStyle = run.Font.Style;

    if (!charStyle.BuiltIn)
        run.Font.Underline = Underline.Double;
}

doc.Save(ArtifactsDir + "Font.Style.docx");
```

### Ver también

* class [Style](../../style/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


