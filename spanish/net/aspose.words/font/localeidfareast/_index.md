---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font LocaleIdFarEast para administrar fácilmente los identificadores de configuración regional para caracteres asiáticos formateados, mejorando sus aplicaciones multilingües.
type: docs
weight: 220
url: /es/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Obtiene o establece el identificador de configuración regional (idioma) de los caracteres asiáticos formateados.

```csharp
public int LocaleIdFarEast { get; set; }
```

## Observaciones

Para obtener la lista de identificadores de configuración regional, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

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

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
