---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.ControlChar pour gérer efficacement les caractères de contrôle dans vos documents pour une mise en forme et une lisibilité améliorées.
type: docs
weight: 550
url: /fr/net/aspose.words/controlchar/
---
## ControlChar class

Caractères de contrôle souvent rencontrés dans les documents.

Pour en savoir plus, visitez le[Travailler avec des caractères de contrôle](https://docs.aspose.com/words/net/working-with-control-characters/) article de documentation.

```csharp
public static class ControlChar
```

## Des champs

| Nom | La description |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | Caractère de fin de cellule ou de fin de ligne de tableau : « \x0007 » ou « \a ». |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | Caractère de fin de cellule ou de fin de ligne de tableau : (char)7 ou "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | Caractère de fin de colonne : « \x000e ». |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | Caractère de fin de colonne : (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Caractère de retour chariot : « \x000d » ou « \r ». Identique à[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Retour chariot suivi d'un caractère de saut de ligne : « \x000d\x000a » ou « \r\n ». Non utilisé comme tel dans les documents Microsoft Word, mais couramment utilisé dans les fichiers texte pour les sauts de paragraphe. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | Il s'agit du caractère « o » utilisé comme valeur par défaut dans les champs de formulaire de saisie de texte. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | Fin du caractère du champ MS Word : (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | Le caractère séparateur de champ sépare le code du champ de sa valeur. Facultatif dans certains champs. Valeur : (car)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | Début du caractère du champ MS Word : (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Caractère de saut de ligne : « \x000a » ou « \n ». Identique à[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Caractère de saut de ligne : « \x000b » ou « \v ». |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Caractère de saut de ligne : (char)11 ou « \v ». |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Caractère de saut de ligne : « \x000a » ou « \n ». Identique à[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Caractère de saut de ligne : (char)10 ou « \n ». |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Le trait d'union insécable dans Microsoft Word est (car)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Caractère espace insécable : « \x00a0 ». |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Caractère espace insécable : (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Le trait d'union facultatif dans Microsoft Word est (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Caractère de saut de page : « \x000c » ou « \f ». Notez que sa valeur est identique à[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Caractère de saut de page : (char)12 ou « \f ». |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | Caractère de fin de paragraphe : « \x000d » ou « \r ». Identique à[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | Caractère de fin de paragraphe : (char)13 ou « \r ». |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | Caractère de fin de section : « \x000c » ou « \f ». Notez que sa valeur est identique à[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | Caractère de fin de section : (char)12 ou « \f ». |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Caractère espace : (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Caractère de tabulation : « \x0009 » ou « \t ». |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Caractère de tabulation : (char)9 ou « \t ». |

## Remarques

fournit les versions char et string des mêmes constantes. Par exemple : string[`LineBreak`](./linebreak/) et char[`LineBreakChar`](./linebreakchar/) ont la même valeur.

## Exemples

Montre comment utiliser les caractères de contrôle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des paragraphes avec du texte avec DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// La conversion du document au format texte révèle que les caractères de contrôle
// représentent certains des éléments structurels du document, tels que les sauts de page.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Lors de la conversion d'un document au format chaîne,
// nous pouvons omettre certains des caractères de contrôle avec la méthode Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
