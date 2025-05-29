---
title: FieldFillIn.PromptText
linktitle: PromptText
articleTitle: PromptText
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldFillIn PromptText, personnalisez facilement les titres des fenêtres d'invite pour améliorer l'expérience utilisateur et améliorer la clarté de l'interface.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldfillin/prompttext/
---
## FieldFillIn.PromptText property

Obtient ou définit le texte de l'invite (le titre de la fenêtre d'invite).

```csharp
public string PromptText { get; set; }
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
