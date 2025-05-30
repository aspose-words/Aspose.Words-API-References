---
title: HtmlSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlSaveOptions ReplaceBackslashWithYenSign mejora su salida HTML al convertir las barras invertidas en símbolos de yen. Valor predeterminado falso.
type: docs
weight: 420
url: /es/net/aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/
---
## HtmlSaveOptions.ReplaceBackslashWithYenSign property

Especifica si los caracteres de barra invertida deben reemplazarse con signos de yen. El valor predeterminado es`FALSO` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Observaciones

De forma predeterminada, Aspose.Words imita el comportamiento de MS Word y no reemplaza las barras invertidas con el signo de yen en los documentos HTML generados. Sin embargo, versiones anteriores de Aspose.Words sí realizaban dichas sustituciones en ciertos casos. Esta opción permite la compatibilidad con versiones anteriores de Aspose.Words.

## Ejemplos

Muestra cómo reemplazar caracteres de barra invertida con signos de yen (HTML).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// De manera predeterminada, Aspose.Words imita el comportamiento de MS Word y no reemplaza los caracteres de barra invertida con signos de yen.
// documentos HTML generados. Sin embargo, versiones anteriores de Aspose.Words realizaban dichas sustituciones en ciertas
// escenarios. Esta bandera permite la compatibilidad con versiones anteriores de Aspose.Words.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
