---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words pour .NET
description: Aspose.Words.ControlChar classe. Caractères de contrôle souvent rencontrés dans les documents en C#.
type: docs
weight: 350
url: /fr/net/aspose.words/controlchar/
---
## ControlChar class

Caractères de contrôle souvent rencontrés dans les documents.

Pour en savoir plus, visitez le[Travailler avec des caractères de contrôle](https://docs.aspose.com/words/net/working-with-control-characters/) article documentaire.

```csharp
public static class ControlChar
```

## Des champs

| Nom | La description |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | Fin de cellule d'un tableau ou caractère de fin de ligne d'un tableau : "\x0007" ou "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | Fin d'une cellule de tableau ou fin d'une ligne de tableau : (char)7 ou "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | Caractère de fin de colonne : "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | Caractère de fin de colonne : (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Caractère de retour chariot : "\x000d" ou "\r". Pareil que[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Retour chariot suivi d'un caractère de saut de ligne : "\x000d\x000a" ou "\r\n". Non utilisé en tant que tel dans les documents Microsoft Word, mais couramment utilisé dans les fichiers texte pour les sauts de paragraphe. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | Il s'agit du caractère "o" utilisé comme valeur par défaut dans les champs du formulaire de saisie de texte. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | Caractère de fin de champ MS Word : (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | Le caractère séparateur de champ sépare le code du champ de la valeur du champ. Facultatif dans certains domaines. Valeur : (car)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | Début du caractère du champ MS Word : (car)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Caractère de saut de ligne : "\x000a" ou "\n". Pareil que[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Caractère de saut de ligne : "\x000b" ou "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Caractère de saut de ligne : (char)11 ou "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Caractère de saut de ligne : "\x000a" ou "\n". Pareil que[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Caractère de saut de ligne : (char)10 ou "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Le trait d'union insécable dans Microsoft Word est (car)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Espace insécable : "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Caractère espace insécable : (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Le trait d'union facultatif dans Microsoft Word est (car)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Caractère de saut de page : "\x000c" ou "\f". Notez qu'il a la même valeur que[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Caractère de saut de page : (char)12 ou "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | Caractère de fin de paragraphe : "\x000d" ou "\r". Pareil que[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | Caractère de fin de paragraphe : (car)13 ou "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | Caractère de fin de section : "\x000c" ou "\f". Notez qu'il a la même valeur que[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | Caractère de fin de section : (car)12 ou "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Caractère espace : (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Caractère de tabulation : "\x0009" ou "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Caractère de tabulation : (char)9 ou "\t". |

## Remarques

Fournit à la fois des versions char et chaîne des mêmes constantes. Par exemple : chaîne[`LineBreak`](./linebreak/) et char[`LineBreakChar`](./linebreakchar/) avoir la même valeur.

## Exemples

Montre comment utiliser les caractères de contrôle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez des paragraphes avec du texte avec DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// La conversion du document sous forme de texte révèle que les caractères de contrôle
// représente certains des éléments structurels du document, tels que les sauts de page.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Lors de la conversion d'un document sous forme de chaîne,
// nous pouvons omettre certains caractères de contrôle avec la méthode Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
