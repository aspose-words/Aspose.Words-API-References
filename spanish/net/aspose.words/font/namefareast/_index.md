---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font NameFarEast para personalizar y configurar fácilmente nombres de fuentes del este de Asia para una tipografía mejorada en sus proyectos.
type: docs
weight: 260
url: /es/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Devuelve o establece un nombre de fuente del este de Asia.

```csharp
public string NameFarEast { get; set; }
```

## Ejemplos

Muestra cómo insertar y formatear texto en un idioma del Lejano Oriente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especifique la configuración de fuente que el generador de documentos aplicará a cualquier texto que inserte.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Nombra equivalentes de "FarEast" para nuestra fuente y configuración regional.
// Si el generador inserta caracteres asiáticos con esta configuración de fuente, entonces cada ejecución que contenga
// estos caracteres se mostrarán utilizando la fuente/configuración regional "FarEast" en lugar de la predeterminada.
// Esto podría ser útil cuando una fuente occidental no tiene representaciones ideales para caracteres asiáticos.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Este texto se mostrará en la fuente/configuración regional predeterminada.
builder.Writeln("Hello world!");

// Dado que se trata de caracteres asiáticos, esta ejecución aplicará nuestros equivalentes de fuente/configuración regional "Lejano Oriente".
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Ver también

* property [Name](../name/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
