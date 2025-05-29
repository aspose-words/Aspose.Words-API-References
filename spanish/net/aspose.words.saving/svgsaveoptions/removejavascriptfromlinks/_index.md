---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words para .NET
description: Optimice archivos SVG con SvgSaveOptions y elimine fácilmente JavaScript de los enlaces para un código más limpio. ¡Mejore el rendimiento y la seguridad con esta sencilla configuración!
type: docs
weight: 60
url: /es/net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

Especifica si se eliminará JavaScript de los enlaces. El valor predeterminado es`FALSO` . Si esta opción está habilitada, todos los enlaces que contengan JavaScript se reemplazarán con "javascript:void(0)".

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Ejemplos

Muestra cómo eliminar JavaScript de los enlaces (svg).

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### Ver también

* class [SvgSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
