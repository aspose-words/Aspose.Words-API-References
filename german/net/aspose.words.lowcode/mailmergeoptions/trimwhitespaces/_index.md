---
title: MailMergeOptions.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Serienbrief mit der TrimWhitespaces-Eigenschaft. Verwalten Sie führende und nachfolgende Leerzeichen ganz einfach für übersichtlichere, professionellere Dokumente.
type: docs
weight: 110
url: /de/net/aspose.words.lowcode/mailmergeoptions/trimwhitespaces/
---
## MailMergeOptions.TrimWhitespaces property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob nachstehende und führende Leerzeichen aus Serienbriefwerten entfernt werden.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` .

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang für einen einzelnen Datensatz durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe zu erstellen:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Siehe auch

* class [MailMergeOptions](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
