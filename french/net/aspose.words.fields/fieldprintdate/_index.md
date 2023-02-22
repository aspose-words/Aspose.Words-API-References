---
title: Class FieldPrintDate
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldPrintDate classe. Implémente le champ PRINTDATE.
type: docs
weight: 2140
url: /fr/net/aspose.words.fields/fieldprintdate/
---
## FieldPrintDate class

Implémente le champ PRINTDATE.

```csharp
public class FieldPrintDate : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldPrintDate](fieldprintdate/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |
| [UseLunarCalendar](../../aspose.words.fields/fieldprintdate/uselunarcalendar/) { get; set; } | Obtient ou définit s'il faut utiliser le calendrier Hijri Lunar ou Hebrew Lunar. |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldprintdate/usesakaeracalendar/) { get; set; } | Obtient ou définit s'il faut utiliser le calendrier Saka Era. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldprintdate/useumalquracalendar/) { get; set; } | Obtient ou définit s'il faut utiliser le calendrier Um-al-Qura. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Récupère la date et l'heure de la dernière impression du document. Par défaut, le calendrier grégorien est utilisé.

### Exemples

Affiche les champs PRINTDATE lus.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Lorsqu'un document est imprimé par une imprimante ou imprimé au format PDF (mais pas exporté au format PDF),
// Les champs PRINTDATE afficheront la date/heure de l'opération d'impression.
// Si aucune impression n'a eu lieu, ces champs afficheront "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Vous trouverez ci-dessous trois types de calendrier différents selon lesquels le champ PRINTDATE
// peut afficher la date et l'heure de la dernière opération d'impression.
// 1 - Calendrier lunaire islamique :
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Calendrier Umm al-Qura :
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Calendrier national indien :
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


