---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words para .NET
description: Descubra si su documento incluye macros de VBA con la propiedad FileFormatInfo HasMacros. ¡Asegure la seguridad y funcionalidad de sus documentos hoy mismo!
type: docs
weight: 30
url: /es/net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

Devuelve`verdadero` Si este documento contiene una macro VBA.

```csharp
public bool HasMacros { get; }
```

## Ejemplos

Muestra cómo comprobar la presencia de una macro VBA sin cargar el documento.

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.IsTrue(fileFormatInfo.HasMacros);
```

### Ver también

* class [FileFormatInfo](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
