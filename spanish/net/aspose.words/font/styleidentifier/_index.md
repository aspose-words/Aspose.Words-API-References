---
title: Font.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font StyleIdentifier para gestionar fácilmente los estilos de carácter en su formato. ¡Mejore su diseño con soluciones que no dependen de la configuración regional!
type: docs
weight: 420
url: /es/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Ejemplos

Muestra cómo cambiar el estilo del texto existente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//A continuación se muestran dos formas de hacer referencia a los estilos.
// 1 - Usando el nombre del estilo:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - Usando un identificador de estilo incorporado:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Convertir todos los usos de un estilo a otro,
// utilizando los métodos anteriores para hacer referencia a estilos antiguos y nuevos.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Ver también

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
