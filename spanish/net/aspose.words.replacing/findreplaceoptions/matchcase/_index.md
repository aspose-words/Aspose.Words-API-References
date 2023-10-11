---
title: FindReplaceOptions.MatchCase
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Verdadero indica una comparación que distingue entre mayúsculas y minúsculas falso indica una comparación que no distingue entre mayúsculas y minúsculas.
type: docs
weight: 140
url: /es/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

Verdadero indica una comparación que distingue entre mayúsculas y minúsculas, falso indica una comparación que no distingue entre mayúsculas y minúsculas.

```csharp
public bool MatchCase { get; set; }
```

### Ejemplos

Muestra cómo alternar la distinción entre mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Podemos utilizar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establece el indicador "MatchCase" en "true" para aplicar distinción entre mayúsculas y minúsculas mientras buscas cadenas para reemplazar.
// Establece el indicador "MatchCase" en "false" para ignorar las mayúsculas y minúsculas mientras buscas texto para reemplazar.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


