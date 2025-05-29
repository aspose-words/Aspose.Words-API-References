---
title: IMailMergeCallback Interface
linktitle: IMailMergeCallback
articleTitle: IMailMergeCallback
second_title: Aspose.Words pour .NET
description: Optimisez votre processus de publipostage avec Aspose.Words.MailMerging.IMailMergeCallback. Recevez des notifications en temps réel et optimisez l'automatisation de vos documents.
type: docs
weight: 4490
url: /fr/net/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface

Implémentez cette interface si vous souhaitez recevoir des notifications pendant l'exécution du publipostage.

```csharp
public interface IMailMergeCallback
```

## Méthodes

| Nom | La description |
| --- | --- |
| [TagsReplaced](../../aspose.words.mailmerging/imailmergecallback/tagsreplaced/)() | Appelé lorsque les balises de texte « moustache » sont remplacées par des champs MERGEFIELD. |

## Exemples

Montre comment définir une logique personnalisée pour la gestion des événements lors du publipostage.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insérer deux balises de publipostage référençant deux colonnes dans une source de données.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Créez une source de données qui contient uniquement une des colonnes référencées par nos balises de fusion.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Configurez notre publipostage pour utiliser des balises de publipostage alternatives.
    doc.MailMerge.UseNonMergeFields = true;

    // Ensuite, assurez-vous que le publipostage convertira les balises, telles que notre balise « LastName »,
    // dans les MERGEFIELD dans les documents de fusion.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Compte le nombre de fois qu'un publipostage remplace les balises de publipostage qu'il n'a pas pu remplir avec des données avec MERGEFIELD.
/// </summary>
private class MailMergeTagReplacementCounter : IMailMergeCallback
{
    public void TagsReplaced()
    {
        TagsReplacedCount++;
    }

    public int TagsReplacedCount { get; private set; }
}
```

### Voir également

* espace de noms [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../)
