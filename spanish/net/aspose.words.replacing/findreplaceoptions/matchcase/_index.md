---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words para .NET
description: Descubra la propiedad MatchCase en FindReplaceOptions y active comparaciones con o sin distinción entre mayúsculas y minúsculas para una edición de texto precisa. ¡Optimice su flujo de trabajo!
type: docs
weight: 140
url: /es/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

Verdadero indica una comparación que distingue entre mayúsculas y minúsculas, falso indica una comparación que no distingue entre mayúsculas y minúsculas.

```csharp
public bool MatchCase { get; set; }
```

## Ejemplos

Muestra cómo alternar la distinción entre mayúsculas y minúsculas al realizar una operación de búsqueda y reemplazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "MatchCase" en "verdadero" para aplicar distinción entre mayúsculas y minúsculas al buscar cadenas para reemplazar.
// Establezca el indicador "MatchCase" en "falso" para ignorar las mayúsculas y minúsculas mientras busca texto para reemplazar.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
