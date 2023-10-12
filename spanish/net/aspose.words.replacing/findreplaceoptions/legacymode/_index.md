---
title: FindReplaceOptions.LegacyMode
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Obtiene o establece un valor booleano que indica que se utiliza el antiguo algoritmo de búsqueda/reemplazo.
type: docs
weight: 130
url: /es/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Obtiene o establece un valor booleano que indica que se utiliza el antiguo algoritmo de búsqueda/reemplazo.

```csharp
public bool LegacyMode { get; set; }
```

### Observaciones

Utilice esta marca si necesita exactamente el mismo comportamiento que antes de que se introdujera la función avanzada de búsqueda/reemplazo. Tenga en cuenta que el algoritmo anterior no admite funciones avanzadas como reemplazar con pausas, aplicar formato, etc.

### Ejemplos

Muestra cómo reconocer y utilizar sustituciones dentro de patrones de reemplazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// El uso del modo heredado no admite muchas funciones avanzadas, por lo que debemos configurarlo en "falso".
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


