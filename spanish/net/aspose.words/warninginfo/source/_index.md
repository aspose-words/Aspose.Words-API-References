---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words para .NET
description: Descubra la propiedad WarningInfo Source que revela el origen de las advertencias, mejorando la confiabilidad de su aplicación y la experiencia del usuario.
type: docs
weight: 20
url: /es/net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

Devuelve la fuente de la advertencia.

```csharp
public WarningSource Source { get; }
```

## Ejemplos

Muestra cómo trabajar con la fuente de advertencia.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Ver también

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
