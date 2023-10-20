---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words para .NET
description: Font NameFarEast propiedad. Devuelve o establece un nombre de fuente de Asia oriental en C#.
type: docs
weight: 260
url: /es/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Devuelve o establece un nombre de fuente de Asia oriental.

```csharp
public string NameFarEast { get; set; }
```

## Ejemplos

Muestra cómo insertar y dar formato a texto en un idioma del Lejano Oriente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especifique la configuración de fuente que el creador de documentos aplicará a cualquier texto que inserte.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Nombre los equivalentes de "FarEast" para nuestra fuente y configuración regional.
// Si el constructor inserta caracteres asiáticos con esta configuración de fuente, entonces cada ejecución que contenga
// estos caracteres los mostrarán usando la fuente/localización "FarEast" en lugar de la predeterminada.
// Esto podría resultar útil cuando una fuente occidental no tiene representaciones ideales para caracteres asiáticos.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Este texto se mostrará en la fuente/localización predeterminada.
builder.Writeln("Hello world!");

// Dado que estos son caracteres asiáticos, esta ejecución aplicará nuestros equivalentes de fuente/localización "FarEast".
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Ver también

* property [Name](../name/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
