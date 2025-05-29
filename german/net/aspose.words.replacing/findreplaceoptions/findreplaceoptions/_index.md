---
title: FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den FindReplaceOptions-Konstruktor, um einfach eine neue Instanz mit Standardeinstellungen zu initialisieren und so Ihre Such- und Ersetzungsfunktionalität zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions() {#constructor}

Initialisiert eine neue Instanz der Klasse FindReplaceOptions mit Standardeinstellungen.

```csharp
public FindReplaceOptions()
```

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

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/)*) {#constructor_1}

Initialisiert eine neue Instanz der Klasse FindReplaceOptions mit der angegebenen Richtung.

```csharp
public FindReplaceOptions(FindReplaceDirection direction)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| direction | FindReplaceDirection | Die Richtung der Such- und Ersetzungsoperation. |

### Siehe auch

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)

---

## FindReplaceOptions(*[IReplacingCallback](../../ireplacingcallback/)*) {#constructor_3}

Initialisiert eine neue Instanz der FindReplaceOptions-Klasse mit dem angegebenen Ersetzungs-Callback.

```csharp
public FindReplaceOptions(IReplacingCallback replacingCallback)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| replacingCallback | IReplacingCallback | Der Rückruf, der zum Ersetzen gefundenen Textes verwendet werden soll. |

## Beispiele

Zeigt, wie die Reihenfolge verfolgt wird, in der ein Textersetzungsvorgang Knoten durchläuft.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // Die Verwendung einer anderen Kopf-/Fußzeile für die erste Seite wirkt sich auf die Suchreihenfolge aus.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Zeichnet während einer Suchen-und-Ersetzen-Operation den Inhalt jedes Knotens auf, der Text enthält, den die Operation „findet“.
/// in dem Zustand, in dem es sich vor dem Austausch befindet.
/// Dadurch wird die Reihenfolge angezeigt, in der der Textersetzungsvorgang die Knoten durchläuft.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### Siehe auch

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/), [IReplacingCallback](../../ireplacingcallback/)*) {#constructor_2}

Initialisiert eine neue Instanz der Klasse FindReplaceOptions mit der angegebenen Richtung und dem Ersetzungs-Callback.

```csharp
public FindReplaceOptions(FindReplaceDirection direction, IReplacingCallback replacingCallback)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| direction | FindReplaceDirection | Die Richtung der Such- und Ersetzungsoperation. |
| replacingCallback | IReplacingCallback | Der Rückruf, der zum Ersetzen gefundenen Textes verwendet werden soll. |

### Siehe auch

* enum [FindReplaceDirection](../../findreplacedirection/)
* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
