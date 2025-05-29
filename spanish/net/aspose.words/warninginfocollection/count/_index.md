---
title: WarningInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad WarningInfoCollection Count para acceder fácilmente al número total de elementos en su colección para una gestión de datos eficiente.
type: docs
weight: 20
url: /es/net/aspose.words/warninginfocollection/count/
---
## WarningInfoCollection.Count property

Obtiene el número de elementos contenidos en la colección.

```csharp
public int Count { get; }
```

## Ejemplos

Muestra cómo obtener advertencias sobre formatos no compatibles.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Ver también

* class [WarningInfoCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
