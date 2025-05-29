---
title: FieldTime Class
linktitle: FieldTime
articleTitle: FieldTime
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldTime pour une implémentation fluide des champs TIME. Optimisez l'automatisation de vos documents grâce à de puissantes fonctionnalités !
type: docs
weight: 2910
url: /fr/net/aspose.words.fields/fieldtime/
---
## FieldTime class

Implémente le champ TIME.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldTime : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldTime](fieldtime/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud immédiatement après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lève une requête si le champ est déjà en cours de mise à jour. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Effectue une mise à jour du champ. L'erreur est générée si le champ est déjà en cours de mise à jour. |

## Remarques

Insère la date et l'heure actuelles.

## Exemples

Montre comment afficher l'heure actuelle à l'aide du champ HEURE.

```csharp
public void FieldTime()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Par défaut, l'heure est affichée au format « h:mm am/pm ».
    FieldTime field = InsertFieldTime(builder, "");

    Assert.AreEqual(" TIME ", field.GetFieldCode());

    // Nous pouvons utiliser l'indicateur \@ pour modifier le format de notre heure affichée.
    field = InsertFieldTime(builder, "\\@ HHmm");

    Assert.AreEqual(" TIME \\@ HHmm", field.GetFieldCode());

    // Nous pouvons ajuster le format pour que le champ TIME affiche également la date, selon le calendrier grégorien.
    field = InsertFieldTime(builder, "\\@ \"M/d/yyyy h mm:ss am/pm\"");

    Assert.AreEqual(" TIME \\@ \"M/d/yyyy h mm:ss am/pm\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.TIME.docx");
}

/// <summary>
/// Utilisez un générateur de documents pour insérer un champ TIME, insérer un nouveau paragraphe et renvoyer le champ.
/// </summary>
private static FieldTime InsertFieldTime(DocumentBuilder builder, string format)
{
    FieldTime field = (FieldTime)builder.InsertField(FieldType.FieldTime, true);
    builder.MoveTo(field.Separator);
    builder.Write(format);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
