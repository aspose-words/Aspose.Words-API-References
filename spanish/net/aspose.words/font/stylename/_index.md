---
title: Font.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font StyleName, administre fácilmente los estilos de caracteres para mejorar el formato de texto y la flexibilidad de diseño en sus proyectos.
type: docs
weight: 430
url: /es/net/aspose.words/font/stylename/
---
## Font.StyleName property

Obtiene o establece el nombre del estilo de carácter aplicado a este formato.

```csharp
public string StyleName { get; set; }
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

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
