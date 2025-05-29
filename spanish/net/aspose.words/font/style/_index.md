---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar la propiedad Estilo de fuente para personalizar los estilos de caracteres en su formato para mejorar el atractivo y la legibilidad del texto.
type: docs
weight: 410
url: /es/net/aspose.words/font/style/
---
## Font.Style property

Obtiene o establece el estilo de carácter aplicado a este formato.

```csharp
public Style Style { get; set; }
```

## Ejemplos

Aplica un subrayado doble a todos los caracteres de un documento que estén formateados con estilos de caracteres personalizados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un estilo personalizado y aplíquelo al texto creado con un generador de documentos.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Itera sobre cada ejecución y agrega un subrayado doble a cada estilo personalizado.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
