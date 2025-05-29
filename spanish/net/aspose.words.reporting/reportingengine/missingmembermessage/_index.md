---
title: ReportingEngine.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words para .NET
description: Descubra la propiedad MissingMemberMessage de ReportingEngine y personalice fácilmente los mensajes para los miembros de objetos faltantes. ¡Mejore la experiencia del usuario sin esfuerzo!
type: docs
weight: 30
url: /es/net/aspose.words.reporting/reportingengine/missingmembermessage/
---
## ReportingEngine.MissingMemberMessage property

Obtiene o establece un valor de cadena impreso en lugar de una expresión de plantilla que representa una referencia simple a un miembro faltante de un objeto. El valor predeterminado es una cadena vacía.

```csharp
public string MissingMemberMessage { get; set; }
```

## Observaciones

La propiedad debe utilizarse junto con laAllowMissingMembers Opción . De lo contrario, se genera una excepción cuando se detecta un miembro faltante de un objeto.

La propiedad solo afecta la impresión de una expresión de plantilla que representa una referencia simple a un miembro del objeto missing . Por ejemplo, la impresión de un operador binario, uno de cuyos operandos hace referencia a un miembro del objeto missing , no se ve afectada.

El valor de esta propiedad no se puede establecer en nulo.

## Ejemplos

Muestra cómo permitir miembros faltantes.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

### Ver también

* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
