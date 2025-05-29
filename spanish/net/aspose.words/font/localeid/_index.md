---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad Font LocaleId mejora el formato de su texto al administrar identificadores de configuración regional para diversos idiomas. ¡Mejore su codificación hoy mismo!
type: docs
weight: 200
url: /es/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Obtiene o establece el identificador de configuración regional (idioma) de los caracteres formateados.

```csharp
public int LocaleId { get; set; }
```

## Observaciones

Para obtener la lista de identificadores de configuración regional, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Ejemplos

Muestra cómo configurar la configuración regional del texto que estamos agregando con un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si establecemos la configuración regional de la fuente en inglés e insertamos algún texto en ruso,
// El corrector ortográfico de la configuración regional en inglés no reconocerá el texto y lo detectará como un error ortográfico.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Establezca una configuración regional coincidente para el texto que estamos a punto de agregar para aplicar el corrector ortográfico adecuado.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
