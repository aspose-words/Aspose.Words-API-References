---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: Aspose.Words för .NET
description: Upptäck hur metoden SetRestrictedTypes i ReportingEngine förbättrar säkerheten genom att begränsa medlemsåtkomst i mallsyntax för optimerad datarapportering.
type: docs
weight: 80
url: /sv/net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

Anger typer, vilka medlemmar samt vilka härledda typers medlemmar som ska vara oåtkomliga för motorn. via mallsyntaxen.

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| types | Type[] | Typer som ska begränsas. |

## Anmärkningar

Begränsade typer bör anges före den allra första versionen av en rapport. Efter`Byggrapport` anropas kan begränsade typer inte ändras och ett undantag utlöses vid försök att göra detta. Det bästa stället att ange begränsade typer är programstart.

Observera att ett stort antal begränsade typer kan påverka prestandan, så det är bättre att bara begränsa de typer vars åtkomst medlemmar är riktigt känslig.

KastarArgumentException i följande fall:

-*types* är noll.

- En av*types* varorna är`null`.

- En av*types* items representerar en osynlig typ, dvs. en icke-publik typ eller en publik kapslad typ som har en icke-publik yttre typ.

- En av*types* items representerar en arraytyp.

-*types* innehåller dubbletter.

## Exempel

Visar hur man nekar åtkomst för medlemmar av typer som anses osäkra.

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// Observera att du inte kan ange begränsade typer under eller efter att du skapat en rapport.
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// Vi ställer in alternativet "AllowMissingMembers" för att undvika undantag när vi skapar en rapport.
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// Vi får en tom sträng eftersom vi inte kan komma åt GetType()-metoden.
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Se även

* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
