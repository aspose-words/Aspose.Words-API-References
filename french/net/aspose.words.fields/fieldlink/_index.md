---
title: Class FieldLink
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldLink classe. Implémente le champ LINK.
type: docs
weight: 1960
url: /fr/net/aspose.words.fields/fieldlink/
---
## FieldLink class

Implémente le champ LINK.

```csharp
public class FieldLink : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldLink](fieldlink/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AutoUpdate](../../aspose.words.fields/fieldlink/autoupdate/) { get; set; } | Obtient ou définit s'il faut mettre à jour ce champ automatiquement. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [FormatUpdateType](../../aspose.words.fields/fieldlink/formatupdatetype/) { get; set; } | Obtient ou définit la façon dont l'objet lié met à jour sa mise en forme. |
| [InsertAsBitmap](../../aspose.words.fields/fieldlink/insertasbitmap/) { get; set; } | Obtient ou définit s'il faut insérer l'objet lié en tant que bitmap. |
| [InsertAsHtml](../../aspose.words.fields/fieldlink/insertashtml/) { get; set; } | Obtient ou définit s'il faut insérer l'objet lié en tant que texte au format HTML. |
| [InsertAsPicture](../../aspose.words.fields/fieldlink/insertaspicture/) { get; set; } | Obtient ou définit s'il faut insérer l'objet lié en tant qu'image. |
| [InsertAsRtf](../../aspose.words.fields/fieldlink/insertasrtf/) { get; set; } | Obtient ou définit s'il faut insérer l'objet lié au format texte enrichi (RTF). |
| [InsertAsText](../../aspose.words.fields/fieldlink/insertastext/) { get; set; } | Obtient ou définit s'il faut insérer l'objet lié au format texte uniquement. |
| [InsertAsUnicode](../../aspose.words.fields/fieldlink/insertasunicode/) { get; set; } | Obtient ou définit s'il faut insérer l'objet lié en tant que texte Unicode. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLinked](../../aspose.words.fields/fieldlink/islinked/) { get; set; } | Obtient ou définit s'il faut réduire la taille du fichier en ne stockant pas les données graphiques avec le document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [ProgId](../../aspose.words.fields/fieldlink/progid/) { get; set; } | Obtient ou définit le type d'application des informations de lien. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [SourceFullName](../../aspose.words.fields/fieldlink/sourcefullname/) { get; set; } | Obtient ou définit le nom et l'emplacement du fichier source. |
| [SourceItem](../../aspose.words.fields/fieldlink/sourceitem/) { get; set; } | Obtient ou définit la partie du fichier source qui est liée. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

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

Pour les informations copiées depuis une autre application, ce champ relie ces informations à son fichier source original .

### Exemples

Montre comment utiliser divers types de champs pour créer des liens vers d'autres documents dans le système de fichiers local et afficher leur contenu.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Vous trouverez ci-dessous trois types de champs que nous pouvons utiliser pour afficher le contenu d'un document lié sous forme de texte.
    // 1 - Un champ LIEN :
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", MyDir + "Document.docx", null, true);

    // 2 - Un champ DDE :
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Un champ DDEAUTO :
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.docx");
}

{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Vous trouverez ci-dessous trois types de champs que nous pouvons utiliser pour afficher le contenu d'un document lié sous la forme d'une image.
    // 1 - Un champ LIEN :
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "MySpreadsheet.xlsx",
        "Sheet1!R2C2", true);

    // 2 - Un champ DDE :
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Un champ DDEAUTO :
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
}

/// <summary>
/// Utilisez un générateur de document pour insérer un champ LINK et définir ses propriétés en fonction de paramètres.
/// </summary>
private static void InsertFieldLink(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool shouldAutoUpdate)
{
    FieldLink field = (FieldLink)builder.InsertField(FieldType.FieldLink, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;

    builder.Writeln("\n");
}

/// <summary>
/// Utilisez un générateur de document pour insérer un champ DDE et définissez ses propriétés en fonction des paramètres.
/// </summary>
private static void InsertFieldDde(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs, string progId,
    string sourceFullName, string sourceItem, bool isLinked, bool shouldAutoUpdate)
{
    FieldDde field = (FieldDde)builder.InsertField(FieldType.FieldDDE, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;

    builder.Writeln("\n");
}

/// <summary>
/// Utilisez un générateur de document pour insérer un champ DDEAUTO, et définissez ses propriétés en fonction de paramètres.
/// </summary>
private static void InsertFieldDdeAuto(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool isLinked)
{
    FieldDdeAuto field = (FieldDdeAuto)builder.InsertField(FieldType.FieldDDEAuto, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;
}

public enum InsertLinkedObjectAs
{
    // ObjetLiéCommeTexte
    Text,
    Unicode,
    Html,
    Rtf,
    // ObjetLiéCommeImage
    Picture,
    Bitmap
}
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


