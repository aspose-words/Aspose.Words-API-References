---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Serienbriefprozess mit der Eigenschaft TrimWhitespaces und sorgen Sie für saubere Daten, indem Sie führende und nachfolgende Leerzeichen entfernen, um genaue Ergebnisse zu erzielen.
type: docs
weight: 130
url: /de/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob nachstehende und führende Leerzeichen aus Serienbriefwerten entfernt werden.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` .

## Beispiele

Zeigt, wie beim Ausführen eines Seriendrucks Leerzeichen aus den Werten einer Datenquelle entfernt werden.

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
