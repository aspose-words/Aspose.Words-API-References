---
title: MailMergerContext.MailMergeOptions
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die MailMergeContext MailMergeOptions-Funktion, um Ihre Dokumentenautomatisierung zu optimieren und die Effizienz Ihres Workflows mühelos zu steigern.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/mailmergercontext/mailmergeoptions/
---
## MailMergerContext.MailMergeOptions property

Seriendruckoptionen.

```csharp
public MailMergeOptions MailMergeOptions { get; }
```

## Beispiele

Zeigt, wie Sie mithilfe des Kontexts einen Serienbriefvorgang für einen einzelnen Datensatz durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe zu erstellen:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Zeigt, wie Sie mithilfe des Kontexts einen Serienbriefvorgang für einen einzelnen Datensatz aus dem Stream durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge mit Dokumenten aus dem Stream durchzuführen:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Siehe auch

* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMergerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
