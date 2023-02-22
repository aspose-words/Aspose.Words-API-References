---
title: MailMerge.TrimWhitespaces
second_title: Aspose.Words für .NET-API-Referenz
description: MailMerge eigendom. Ruft einen Wert ab oder legt einen Wert fest der angibt ob nachgestellte und führende Leerzeichen aus Serienbriefwerten entfernt werden.
type: docs
weight: 130
url: /de/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob nachgestellte und führende Leerzeichen aus Serienbriefwerten entfernt werden.

```csharp
public bool TrimWhitespaces { get; set; }
```

### Bemerkungen

Der Standardwert ist **Stimmt** .

### Beispiele

Zeigt, wie Leerzeichen aus Werten einer Datenquelle entfernt werden, während ein Seriendruck ausgeführt wird.

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
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)


