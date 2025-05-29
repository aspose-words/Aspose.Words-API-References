---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words para .NET
description: Descubra la propiedad IdPrefix de HtmlFixedSaveOptions para personalizar los ID de los elementos en sus documentos. ¡Mejore la organización con prefijos personalizados para un mejor resultado!
type: docs
weight: 100
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

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

Muestra cómo agregar un prefijo que se antepone a todos los ID de elementos generados.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
