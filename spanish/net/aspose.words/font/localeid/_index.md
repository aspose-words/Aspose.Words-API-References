---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words para .NET
description: Font LocaleId propiedad. Obtiene o establece el identificador local idioma de los caracteres formateados en C#.
type: docs
weight: 200
url: /es/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Obtiene o establece el identificador local (idioma) de los caracteres formateados.

```csharp
public int LocaleId { get; set; }
```

## Observaciones

Para obtener la lista de identificadores locales, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Ejemplos

Muestra cómo configurar la configuración regional del texto que estamos agregando con un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si configuramos la configuración regional de la fuente en inglés e insertamos texto en ruso,
// el corrector ortográfico local en inglés no reconocerá el texto y lo detectará como un error ortográfico.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Establece una configuración regional coincidente para el texto que estamos a punto de agregar para aplicar el corrector ortográfico apropiado.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
