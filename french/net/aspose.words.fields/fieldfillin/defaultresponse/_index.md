---
title: FieldFillIn.DefaultResponse
linktitle: DefaultResponse
articleTitle: DefaultResponse
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldFillIn DefaultResponse pour définir et personnaliser facilement les réponses utilisateur par défaut dans les fenêtres d'invite pour une expérience utilisateur améliorée.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldfillin/defaultresponse/
---
## FieldFillIn.DefaultResponse property

Obtient ou définit la réponse utilisateur par défaut (valeur initiale contenue dans la fenêtre d'invite).

```csharp
public string DefaultResponse { get; set; }
```

## Exemples

Montre comment utiliser le champ REMPLIR pour demander à l'utilisateur une réponse.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insérer un champ de type « REMPLISSAGE ». Lorsque nous mettons à jour ce champ manuellement dans Microsoft Word,
    // Il nous sera demandé de saisir une réponse. Le champ affichera alors la réponse sous forme de texte.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Nous pouvons également utiliser ces champs pour demander à l'utilisateur une réponse unique pour chaque page
    // créé lors d'un publipostage effectué à l'aide de Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Si nous effectuons un publipostage par programmation, nous pouvons utiliser un répondeur d'invite personnalisé
    // pour modifier automatiquement les réponses pour les champs FILLIN rencontrés par le publipostage.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// Ajoute une ligne à la réponse par défaut de chaque champ FILLIN lors d'un publipostage.
/// </summary>
private class PromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response modified by PromptRespondent. " + defaultResponse;
    }
}
```

### Voir également

* class [FieldFillIn](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
