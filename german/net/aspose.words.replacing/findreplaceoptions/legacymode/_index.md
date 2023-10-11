---
title: FindReplaceOptions.LegacyMode
second_title: Aspose.Words für .NET-API-Referenz
description: FindReplaceOptions eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt dass der alte Such/Ersetzungsalgorithmus verwendet wird.
type: docs
weight: 130
url: /de/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, dass der alte Such-/Ersetzungsalgorithmus verwendet wird.

```csharp
public bool LegacyMode { get; set; }
```

### Bemerkungen

Verwenden Sie dieses Flag, wenn Sie genau das gleiche Verhalten wie vor der Einführung der erweiterten Such-/Ersetzungsfunktion benötigen. Beachten Sie, dass der alte Algorithmus keine erweiterten Funktionen wie das Ersetzen durch Umbrüche, das Anwenden von Formatierungen usw. unterstützt.

### Beispiele

Zeigt, wie Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Die Verwendung des Legacy-Modus unterstützt viele erweiterte Funktionen nicht, daher müssen wir ihn auf „false“ setzen.
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../findreplaceoptions/)
* Montage [Aspose.Words](../../../)


