---
title: FindReplaceOptions.LegacyMode
linktitle: LegacyMode
articleTitle: LegacyMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die LegacyMode-Eigenschaft von FindReplaceOptions, um den klassischen Suchen/Ersetzen-Algorithmus für erweiterte Funktionalität und ein nahtloses Benutzererlebnis einfach umzuschalten.
type: docs
weight: 130
url: /de/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, dass der alte Suchen/Ersetzen-Algorithmus verwendet wird.

```csharp
public bool LegacyMode { get; set; }
```

## Bemerkungen

Verwenden Sie dieses Flag, wenn Sie genau dasselbe Verhalten wie vor der Einführung der erweiterten Suchen/Ersetzen-Funktion benötigen. Beachten Sie, dass der alte Algorithmus keine erweiterten Funktionen wie Ersetzen durch Umbrüche, Formatierung anwenden usw. unterstützt.

## Beispiele

Zeigt, wie man Ersetzungen innerhalb von Ersetzungsmustern erkennt und verwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Die Verwendung des Legacy-Modus unterstützt nicht viele erweiterte Funktionen, daher müssen wir ihn auf „false“ setzen.
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
