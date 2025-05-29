---
title: FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words för .NET
description: Upptäck FindReplaceOptions-konstruktorn för att enkelt initiera en ny instans med standardinställningar, vilket förbättrar din sök- och ersättningsfunktionalitet.
type: docs
weight: 10
url: /sv/net/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions() {#constructor}

Initierar en ny instans av FindReplaceOptions-klassen med standardinställningar.

```csharp
public FindReplaceOptions()
```

## Exempel

Visar hur man känner igen och använder substitutioner inom ersättningsmönster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Att använda äldre läge har inte stöd för många avancerade funktioner, så vi måste ställa in det på 'false'.
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/)*) {#constructor_1}

Initierar en ny instans av FindReplaceOptions-klassen med den angivna riktningen.

```csharp
public FindReplaceOptions(FindReplaceDirection direction)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| direction | FindReplaceDirection | Riktningen för sök- och ersättningsåtgärden. |

### Se även

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)

---

## FindReplaceOptions(*[IReplacingCallback](../../ireplacingcallback/)*) {#constructor_3}

Initierar en ny instans av FindReplaceOptions-klassen med den angivna ersättningsanropsfunktionen.

```csharp
public FindReplaceOptions(IReplacingCallback replacingCallback)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| replacingCallback | IReplacingCallback | Återanropet som ska användas för att ersätta hittad text. |

## Exempel

Visar hur man spårar i vilken ordning en textersättningsoperation passerar noder.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // Att använda ett annat sidhuvud/sidfot för första sidan påverkar sökordningen.
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
/// Under en sök-och-ersätt-operation registreras innehållet i varje nod som har text som operationen 'hittar',
/// i det tillstånd den är i innan utbytet sker.
/// Detta visar i vilken ordning textersättningsoperationen passerar noder.
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

### Se även

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/), [IReplacingCallback](../../ireplacingcallback/)*) {#constructor_2}

Initierar en ny instans av FindReplaceOptions-klassen med den angivna riktningen och ersättande callback.

```csharp
public FindReplaceOptions(FindReplaceDirection direction, IReplacingCallback replacingCallback)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| direction | FindReplaceDirection | Riktningen för sök- och ersättningsåtgärden. |
| replacingCallback | IReplacingCallback | Återanropet som ska användas för att ersätta hittad text. |

### Se även

* enum [FindReplaceDirection](../../findreplacedirection/)
* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
