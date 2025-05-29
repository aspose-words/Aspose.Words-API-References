---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: Aspose.Words för .NET
description: Upptäck om stöd för dubbelriktad text är aktiverat i FieldOptions. Hantera enkelt textuppdateringar för förbättrad flerspråkig funktionalitet.
type: docs
weight: 150
url: /sv/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Hämtar eller ställer in värdet som anger om dubbelriktad text stöds fullt ut under fältuppdatering eller inte.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## Anmärkningar

När den här egenskapen är inställd på`sann`, ytterligare steg utförs för att producera ett fältresultat som är kompatibelt med höger-till-vänster (dvs. arabiska eller hebreiska) under uppdateringen.

När den här egenskapen är inställd på`falsk` och höger-till-vänster-språk används, garanteras inte att fältet result är korrekt efter uppdateringen.

Standardvärdet är`falsk`.

## Exempel

Visar hur man använder FieldOptions för att säkerställa att fältuppdatering har fullt stöd för dubbelriktad text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Se till att alla fältoperationer som involverar text från höger till vänster utförs som förväntat.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Använd en dokumentbyggare för att infoga ett fält som innehåller text från höger till vänster.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Se även

* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
