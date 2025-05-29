---
title: HtmlSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words para .NET
description: Optimice su contenido web con HtmlSaveOptions para eliminar fácilmente JavaScript de los enlaces, mejorando el rendimiento y la experiencia del usuario.
type: docs
weight: 410
url: /es/net/aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/
---
## HtmlSaveOptions.RemoveJavaScriptFromLinks property

Especifica si se eliminará JavaScript de los enlaces. El valor predeterminado es`FALSO` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Observaciones

Si esta opción está habilitada, todos los enlaces que contengan JavaScript (por ejemplo, los enlaces con "javascript:" en el atributo href) se reemplazarán por "javascript:void(0)". Esto puede ayudar a prevenir posibles riesgos de seguridad, como ataques XSS.

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
