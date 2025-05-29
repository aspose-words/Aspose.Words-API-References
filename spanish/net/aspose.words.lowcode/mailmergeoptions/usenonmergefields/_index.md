---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words para .NET
description: Desbloquee funciones avanzadas de combinación de correspondencia con la propiedad UseNonMergeFields. Integre fácilmente MERGEFIELD y otros tipos de campos para una mejor personalización de documentos.
type: docs
weight: 130
url: /es/net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

Cuando`verdadero` , especifica que además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en las etiquetas "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

## Observaciones

Normalmente, la combinación de correspondencia solo se realiza en los campos MERGEFIELD, pero varios clientes crearon su reporting con otros campos y muchos documentos de esta manera. Para simplificar la migración (y dado que varios clientes utilizaron este enfoque de forma independiente), se introdujo la posibilidad de combinar correspondencia en otros campos.

Cuando`UseNonMergeFields` está configurado para`verdadero`Aspose.Words realizará la combinación de correspondencia en los siguientes campos:

MERGEFIELD Nombre del campo

MACROBOTÓN NOMACRO Nombre del campo

SI 0 = 0 "{NombreDeCampo}" ""

Además, cuando`UseNonMergeFields` está configurado para`verdadero`Aspose.Words combinará correspondencia en etiquetas de texto "{{fieldName}}". Estas no son campos, sino etiquetas de texto.

### Ver también

* class [MailMergeOptions](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
