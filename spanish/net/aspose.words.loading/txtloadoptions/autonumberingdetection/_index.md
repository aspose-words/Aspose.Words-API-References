---
title: TxtLoadOptions.AutoNumberingDetection
second_title: Referencia de API de Aspose.Words para .NET
description: TxtLoadOptions propiedad. Obtiene o establece un valor booleano que indica que se realizará la detección de numeración automática mientras se carga un documento. El valor predeterminado esverdadero .
type: docs
weight: 20
url: /es/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Obtiene o establece un valor booleano que indica que se realizará la detección de numeración automática mientras se carga un documento. El valor predeterminado es`verdadero` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

### Ejemplos

Muestra cómo desactivar la detección automática de numeración.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Ver también

* class [TxtLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../txtloadoptions/)
* asamblea [Aspose.Words](../../../)


