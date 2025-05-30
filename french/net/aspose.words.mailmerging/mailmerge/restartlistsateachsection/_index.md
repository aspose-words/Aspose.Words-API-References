---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MailMerge RestartListsAtEachSection  la liste de contrôle se réinitialise dans chaque section pour des publipostages fluides. Améliorez la précision de vos documents dès aujourd'hui !
type: docs
weight: 110
url: /fr/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Obtient ou définit une valeur indiquant si les listes sont redémarrées à chaque section après l'exécution d'un publipostage.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Remarques

La valeur par défaut est`vrai` .

## Exemples

Montre comment contrôler si la numérotation de la liste est redémarrée ou non à chaque section lorsque le publipostage est effectué.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
