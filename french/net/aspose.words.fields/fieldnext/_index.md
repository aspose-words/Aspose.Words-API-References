---
title: FieldNext Class
linktitle: FieldNext
articleTitle: FieldNext
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldNext pour gérer efficacement les champs NEXT dans vos documents. Optimisez l'automatisation de vos documents dès aujourd'hui !
type: docs
weight: 2590
url: /fr/net/aspose.words.fields/fieldnext/
---
## FieldNext class

Implémente le champ NEXT.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldNext : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldNext](fieldnext/)() | Default_Constructor |

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

Fusionne l'enregistrement de données suivant dans le document fusionné résultant actuel, plutôt que de démarrer un nouveau document fusionné.

## Exemples

Montre comment utiliser les champs NEXT/NEXTIF pour fusionner plusieurs lignes en une seule page lors d'un publipostage.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Créez une source de données pour notre publipostage avec 3 lignes.
    // Un publipostage qui utilise cette table créerait normalement un document de 3 pages.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Si nous avons plusieurs champs de fusion avec le même FieldName,
    // ils recevront des données de la même ligne de la source de données et afficheront la même valeur après la fusion.
    // Un champ NEXT indique instantanément au publipostage de descendre d'une ligne,
    // ce qui signifie que tous les MERGEFIELD qui suivent le champ NEXT recevront les données de la ligne suivante.
    // Assurez-vous de ne jamais essayer de passer à la ligne suivante alors que vous êtes déjà sur la dernière ligne.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Après la fusion, les valeurs de la source de données que ces MERGEFIELD acceptent
     // finira sur la même page que les MERGEFIELD ci-dessus.
    InsertMergeFields(builder, "Second row: ");

    // Un champ NEXTIF a la même fonction qu'un champ NEXT,
    // mais il passe à la ligne suivante uniquement si une instruction construite par les 3 propriétés suivantes est vraie.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Si la comparaison affirmée par le champ ci-dessus est correcte,
    // les 3 champs de fusion suivants prendront les données de la troisième ligne.
    // Sinon, ces champs reprendront les données de la ligne 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // Notre source de données comporte 3 lignes et nous avons ignoré des lignes deux fois.
    // Notre document de sortie comportera 1 page avec les données des 3 lignes.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Utilise un générateur de documents pour insérer des MERGEFIELD pour une source de données contenant des colonnes nommées « Titre de courtoisie », « Prénom » et « Nom de famille ».
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Utilise un générateur de documents pour insérer un MERRGEFIELD avec des propriétés spécifiées.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
