---
title: MailMerge.RestartListsAtEachSection
second_title: Référence de l'API Aspose.Words pour .NET
description: MailMerge propriété. Obtient ou définit une valeur indiquant si les listes sont redémarrées à chaque section après lexécution dun publipostage.
type: docs
weight: 110
url: /fr/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Obtient ou définit une valeur indiquant si les listes sont redémarrées à chaque section après l'exécution d'un publipostage.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

### Remarques

La valeur par défaut est`vrai` .

### Exemples

Montre comment contrôler si la numérotation des listes est redémarrée ou non à chaque section lors de la fusion et du publipostage.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)


