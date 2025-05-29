---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words für .NET
description: Nutzen Sie erweiterte Serienbrieffunktionen mit der Eigenschaft „UseNonMergeFields“. Integrieren Sie MERGEFIELD und andere Feldtypen nahtlos für eine verbesserte Dokumentanpassung.
type: docs
weight: 130
url: /de/net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

Wann`WAHR` , gibt an, dass Serienbriefe zusätzlich zu MERGEFIELD-Feldern auch in einigen anderen Feldtypen und auch in "{{fieldName}}"-Tags ausgeführt werden.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Bemerkungen

Normalerweise wird Serienbriefe nur in MERGEFIELD-Feldern ausgeführt, aber einige Kunden hatten ihre Berichte mit anderen Feldern erstellt und viele Dokumente auf diese Weise erstellt. Um die Migration zu vereinfachen (und weil dieser -Ansatz von mehreren Kunden unabhängig voneinander genutzt wurde), wurde die Möglichkeit eingeführt, Serienbriefe in andere Felder zu übertragen.

Wann`UseNonMergeFields` ist eingestellt auf`WAHR`, Aspose.Words führt Serienbriefe in den folgenden Feldern durch:

MERGEFIELD Feldname

MACROBUTTON NOMACRO Feldname

WENN 0 = 0 "{Feldname}" ""

Auch wenn`UseNonMergeFields` ist eingestellt auf`WAHR`Aspose.Words führt Serienbriefe in Text-Tags "{{fieldName}}" durch. Dabei handelt es sich nicht um Felder, sondern lediglich um Text-Tags.

### Siehe auch

* class [MailMergeOptions](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
