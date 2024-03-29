---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words für .NET
description: MailMerge TrimWhitespaces eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob nachgestellte und führende Leerzeichen aus Serienbriefwerten entfernt werden in C#.
type: docs
weight: 130
url: /de/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob nachgestellte und führende Leerzeichen aus Serienbriefwerten entfernt werden.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` .

## Beispiele

Zeigt, wie Leerzeichen aus Werten einer Datenquelle entfernt werden, während ein Serienbrief ausgeführt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.AreEqual(trimWhitespaces ? "hello world!\f" : "\t hello world! \f", doc.GetText());
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
