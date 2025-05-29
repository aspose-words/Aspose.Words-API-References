---
title: MailMergerContext.MailMergeOptions
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words pour .NET
description: Découvrez la fonctionnalité MailMergeContext MailMergeOptions pour rationaliser l'automatisation de vos documents et améliorer l'efficacité de votre flux de travail sans effort.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/mailmergercontext/mailmergeoptions/
---
## MailMergerContext.MailMergeOptions property

Options de publipostage.

```csharp
public MailMergeOptions MailMergeOptions { get; }
```

## Exemples

Montre comment effectuer une opération de publipostage pour un seul enregistrement à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage :
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

Montre comment effectuer une opération de publipostage pour un seul enregistrement du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à l'aide de documents du flux :
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

### Voir également

* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMergerContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
