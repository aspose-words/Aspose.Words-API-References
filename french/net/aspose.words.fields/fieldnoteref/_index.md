---
title: Class FieldNoteRef
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldNoteRef classe. Implémente le champ NOTEREF.
type: docs
weight: 2050
url: /fr/net/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class

Implémente le champ NOTEREF.

```csharp
public class FieldNoteRef : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldNoteRef](fieldnoteref/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldnoteref/bookmarkname/) { get; set; } | Obtient ou définit le nom du signet. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [InsertHyperlink](../../aspose.words.fields/fieldnoteref/inserthyperlink/) { get; set; } | Obtient ou définit s'il faut insérer un lien hypertexte vers le paragraphe marqué d'un signet. |
| [InsertReferenceMark](../../aspose.words.fields/fieldnoteref/insertreferencemark/) { get; set; } | Insère la marque de référence avec le même format de caractère que le style Footnote Reference ou Endnote Reference. |
| [InsertRelativePosition](../../aspose.words.fields/fieldnoteref/insertrelativeposition/) { get; set; } | Obtient ou définit s'il faut insérer une position relative du paragraphe marqué d'un signet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
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

Insère la marque de la note de bas de page ou de la note de fin marquée par le signet spécifié.

### Exemples

Affiche pour insérer des champs NOTEREF et modifier leur apparence.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crée un signet avec une note de bas de page que le champ NOTEREF référencera.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Ce champ NOTEREF affichera le numéro de la note de bas de page à l'intérieur du signet référencé.
    // La définition de la propriété InsertHyperlink nous permet d'accéder au signet par Ctrl + clic sur le champ dans Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // Lors de l'utilisation du drapeau \p, après le numéro de la note de bas de page, le champ affiche également la position du signet par rapport au champ.
    // Bookmark1 est au-dessus de ce champ et contient la note de bas de page numéro 1, donc le résultat sera "1 au-dessus" lors de la mise à jour.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 est sous ce champ et contient la note de bas de page numéro 2, donc le champ affichera "2 ci-dessous".
    // Le drapeau \f fait apparaître le numéro 2 dans le même format que l'étiquette du numéro de note de bas de page dans le texte réel.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");

/// <summary>
/// Utilise un générateur de document pour insérer un champ NOTEREF avec les propriétés spécifiées.
/// </summary>
private static FieldNoteRef InsertFieldNoteRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, bool insertReferenceMark, string textBefore)
{
    builder.Write(textBefore);

    FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    field.InsertReferenceMark = insertReferenceMark;
    builder.Writeln();

    return field;
}

/// <summary>
/// Utilise un générateur de document pour insérer un signet nommé avec une note de bas de page à la fin.
/// </summary>
private static void InsertBookmarkWithFootnote(DocumentBuilder builder, string bookmarkName, string bookmarkText, string footnoteText)
{
    builder.StartBookmark(bookmarkName);
    builder.Write(bookmarkText);
    builder.InsertFootnote(FootnoteType.Footnote, footnoteText);
    builder.EndBookmark(bookmarkName);
    builder.Writeln();
}
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


