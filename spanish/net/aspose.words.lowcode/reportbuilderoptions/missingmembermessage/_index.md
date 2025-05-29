---
title: ReportBuilderOptions.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words para .NET
description: Descubra la propiedad MissingMemberMessage de ReportBuilderOptions. Personalice fácilmente los mensajes para las referencias a objetos faltantes, mejorando la experiencia del usuario sin esfuerzo.
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/reportbuilderoptions/missingmembermessage/
---
## ReportBuilderOptions.MissingMemberMessage property

Obtiene o establece un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. El valor predeterminado es una cadena vacía.

```csharp
public string MissingMemberMessage { get; set; }
```

## Observaciones

La propiedad debe utilizarse junto con laAllowMissingMembers Opción . De lo contrario, se genera una excepción cuando se detecta un miembro faltante de un objeto.

La propiedad solo afecta la impresión de una expresión de plantilla que representa una referencia simple a un miembro del objeto missing . Por ejemplo, la impresión de un operador binario, uno de cuyos operandos hace referencia a un miembro del objeto missing , no se ve afectada.

El valor de esta propiedad no se puede establecer en nulo.

### Ver también

* class [ReportBuilderOptions](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
