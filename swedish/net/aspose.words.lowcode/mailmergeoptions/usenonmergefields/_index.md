---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words för .NET
description: Lås upp avancerade funktioner för dokumentkoppling med egenskapen UseNonMergeFields. Integrera MERGEFIELD och andra fälttyper sömlöst för förbättrad dokumentanpassning.
type: docs
weight: 130
url: /sv/net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

När`sann` , anger att utöver MERGEFIELD-fält utförs dokumentkoppling i vissa andra typer av fält och även i "{{fieldName}}"-taggar.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Anmärkningar

Normalt sett utförs dokumentkoppling endast i MERGEFIELD-fält, men flera kunder har byggt sina reporting med hjälp av andra fält och har skapat många dokument på det här sättet. För att förenkla migreringen (och eftersom denna -metod användes oberoende av varandra av flera kunder) introducerades möjligheten att koppla dokument till andra fält.

När`UseNonMergeFields` är inställd på`sann`Aspose.Words kommer att utföra dokumentkopplingar i följande fält:

MERGEFIELD Fältnamn

MAKROKNAPP NOMACRO Fältnamn

OM 0 = 0 "{Fältnamn}" ""

Även när`UseNonMergeFields` är inställd på`sann`Aspose.Words kommer att utföra dokumentkoppling till text tags "{{fieldName}}". Dessa är inte fält, utan bara texttaggar.

### Se även

* class [MailMergeOptions](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
