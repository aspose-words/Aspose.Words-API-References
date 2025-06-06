---
title: FieldDate Class
linktitle: FieldDate
articleTitle: FieldDate
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldDate, conçue pour implémenter sans effort les champs DATE, améliorant ainsi l'automatisation et le formatage de vos documents.
type: docs
weight: 2180
url: /fr/net/aspose.words.fields/fielddate/
---
## FieldDate class

Implémente le champ DATE.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldDate : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldDate](fielddate/)() | Default_Constructor |

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
| [UseLastFormat](../../aspose.words.fields/fielddate/uselastformat/) { get; set; } | Obtient ou définit s'il faut utiliser un format utilisé en dernier par l'application d'hébergement lors de l'insertion d'un nouveau champ DATE. |
| [UseLunarCalendar](../../aspose.words.fields/fielddate/uselunarcalendar/) { get; set; } | Obtient ou définit s'il faut utiliser le calendrier lunaire hégirien ou lunaire hébreu. |
| [UseSakaEraCalendar](../../aspose.words.fields/fielddate/usesakaeracalendar/) { get; set; } | Obtient ou définit s'il faut utiliser le calendrier de l'ère Saka. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fielddate/useumalquracalendar/) { get; set; } | Obtient ou définit s'il faut utiliser le calendrier Um-al-Qura. |

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

Insère la date et l'heure actuelles. Par défaut, le calendrier grégorien est utilisé.

## Exemples

Montre comment utiliser les champs DATE pour afficher les dates selon différents types de calendriers.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous voulons que le texte du document affiche toujours la date correcte, nous pouvons utiliser un champ DATE.
// Vous trouverez ci-dessous trois types de calendriers culturels qu'un champ DATE peut utiliser pour afficher une date.
// 1 - Calendrier lunaire islamique :
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Calendrier d'Umm al-Qura :
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Calendrier national indien :
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Insérez un champ DATE et définissez son type de calendrier sur celui utilisé en dernier par l'application hôte.
// Dans Microsoft Word, le type sera le plus récemment utilisé dans la boîte de dialogue Insérer -> Texte -> Date et heure.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
