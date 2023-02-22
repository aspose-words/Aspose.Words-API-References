---
title: FindReplaceOptions.MatchCase
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Verdadero indica una comparación que distingue entre mayúsculas y minúsculas falso indica una comparación que no distingue entre mayúsculas y minúsculas.
type: docs
weight: 120
url: /es/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

Verdadero indica una comparación que distingue entre mayúsculas y minúsculas, falso indica una comparación que no distingue entre mayúsculas y minúsculas.

```csharp
public bool MatchCase { get; set; }
```

### Ejemplos

Muestra cómo alternar entre mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "MatchCase" en "verdadero" para aplicar la distinción entre mayúsculas y minúsculas mientras busca cadenas para reemplazar.
// Establezca el indicador "MatchCase" en "falso" para ignorar las mayúsculas y minúsculas mientras busca texto para reemplazar.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


