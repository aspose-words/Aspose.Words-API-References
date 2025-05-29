---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words para .NET
description: Descubra la propiedad IdPrefix de SvgSaveOptions, que personaliza los ID de los elementos en su documento de salida para una mejor organización y claridad. ¡Mejore sus archivos SVG hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

Especifica un prefijo que se antepone a todos los ID de elementos generados en el documento de salida. El valor predeterminado es nulo y no se antepone ningún prefijo.

```csharp
public string IdPrefix { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentException | El valor no cumple los requisitos especificados anteriormente. |

## Observaciones

Si se especifica el prefijo, éste solo puede contener letras, dígitos, guiones bajos y guiones, y debe comenzar con una letra.

## Ejemplos

Muestra cómo agregar un prefijo que se antepone a todos los ID de elementos generados (svg).

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### Ver también

* class [SvgSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
