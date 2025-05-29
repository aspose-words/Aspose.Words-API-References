---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words para .NET
description: Optimice su HTML con la función HtmlFixedSaveOptions RemoveJavaScriptFromLinks. Mejore la seguridad eliminando JavaScript de los enlaces fácilmente.
type: docs
weight: 140
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

Especifica si se eliminará JavaScript de los enlaces. El valor predeterminado es`FALSO` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Observaciones

Si esta opción está habilitada, todos los enlaces que contengan JavaScript (por ejemplo, los enlaces con "javascript:" en el atributo href) se reemplazarán por "javascript:void(0)". Esto puede ayudar a prevenir posibles riesgos de seguridad, como ataques XSS.

## Ejemplos

Muestra cómo eliminar JavaScript de los enlaces.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

Muestra cómo eliminar JavaScript de los enlaces a documentos HTML corregidos.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
