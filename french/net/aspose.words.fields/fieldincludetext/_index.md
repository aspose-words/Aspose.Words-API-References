---
title: Class FieldIncludeText
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fields.FieldIncludeText classe. Implémente le champ INCLUDETEXT.
type: docs
weight: 1900
url: /fr/net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

Implémente le champ INCLUDETEXT.

```csharp
public class FieldIncludeText : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldIncludeText](fieldincludetext/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname/) { get; set; } | Obtient ou définit le nom du signet dans le document à inclure. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding/) { get; set; } | Obtient ou définit l'encodage appliqué aux données dans le fichier référencé. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields/) { get; set; } | Obtient ou définit s'il faut empêcher la mise à jour des champs du document inclus. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype/) { get; set; } | Obtient ou définit le type MIME du fichier référencé. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings/) { get; set; } | Obtient ou définit les mappages d'espace de noms pour les requêtes XPath. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname/) { get; set; } | Obtient ou définit l'emplacement du document à l'aide d'un IRI. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter/) { get; set; } | Obtient ou définit le nom du convertisseur de texte pour le format du fichier inclus. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath/) { get; set; } | Obtient ou définit XPath pour la partie souhaitée du fichier XML. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation/) { get; set; } | Obtient ou définit l'emplacement de la transformation XSL pour formater les données XML. |

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

Insère tout ou partie du texte et des graphiques contenus dans un autre document.

### Exemples

Montre comment créer un champ INCLUDETEXT et définir ses propriétés.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Vous trouverez ci-dessous deux manières d'utiliser les champs INCLUDETEXT pour afficher le contenu d'un fichier XML dans le système de fichiers local.
    // 1 - Effectuez une transformation XSL sur un document XML :
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Utilisez un XPath pour prendre des éléments spécifiques d'un document XML :
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");

/// <summary>
/// Utilisez un générateur de document pour insérer un champ INCLUDETEXT avec des propriétés personnalisées.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)


