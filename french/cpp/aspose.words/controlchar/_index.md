---
title: "classe Aspose::Words::ControlChar"
linktitle: "ControlChar"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::ControlChar. Les caractères de contrôle sont souvent rencontrés dans les documents. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words/controlchar/
---
## ControlChar class


Caractères de contrôle souvent rencontrés dans les documents. Pour en savoir plus, consultez l'article de documentation [Working With Control Characters](https://docs.aspose.com/words/cpp/working-with-control-characters/).

```cpp
class ControlChar
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [Cell](./cell/)() | Caractère de fin de cellule de tableau ou de fin de ligne de tableau : "\x0007" ou "\a". |
| static [ColumnBreak](./columnbreak/)() | Caractère de fin de colonne : "\x000e". |
| [ControlChar](./controlchar/)() |  |
| static [Cr](./cr/)() | Caractère de retour chariot : "\x000d" ou "\r". Identique à [ParagraphBreak](./paragraphbreak/). |
| static [CrLf](./crlf/)() | Caractère de retour chariot suivi d'un saut de ligne : "\x000d\x000a" ou "\r\n". Non utilisé de cette façon dans les documents Microsoft Word, mais couramment utilisé dans les fichiers texte pour les sauts de paragraphe. |
| static [Lf](./lf/)() | Caractère de saut de ligne : "\x000a" ou "\n". Identique à [LineFeed](./linefeed/). |
| static [LineBreak](./linebreak/)() | Caractère de saut de ligne : "\x000b" ou "\v". |
| static [LineFeed](./linefeed/)() | Caractère de saut de ligne : "\x000a" ou "\n". Identique à [Lf](./lf/). |
| static [NonBreakingSpace](./nonbreakingspace/)() | Caractère d'espace insécable : "\x00a0". |
| static [PageBreak](./pagebreak/)() | Caractère de saut de page : "\x000c" ou "\f". Notez qu'il a la même valeur que [SectionBreak](./sectionbreak/). |
| static [ParagraphBreak](./paragraphbreak/)() | Caractère de fin de paragraphe : "\x000d" ou "\r". Identique à [Cr](./cr/) |
| static [SectionBreak](./sectionbreak/)() | Caractère de fin de section : "\x000c" ou "\f". Notez qu'il a la même valeur que [PageBreak](./pagebreak/). |
| static [Tab](./tab/)() | Caractère de tabulation : "\x0009" ou "\t". |
## Champs

| Champ | Description |
| --- | --- |
| static constexpr [CellChar](./cellchar/) | Caractère de fin de cellule de tableau ou de fin de ligne de tableau : (char)7 ou "\a". |
| static constexpr [ColumnBreakChar](./columnbreakchar/) | Caractère de fin de colonne : (char)14. |
| static constexpr [DefaultTextInputChar](./defaulttextinputchar/) | Ceci est le caractère "o" utilisé comme valeur par défaut dans les champs de formulaire de saisie de texte. |
| static constexpr [FieldEndChar](./fieldendchar/) | Caractère de fin de champ MS Word : (char)21. |
| static constexpr [FieldSeparatorChar](./fieldseparatorchar/) | Le caractère séparateur de champ sépare le code du champ de la valeur du champ. Optionnel dans certains champs. Valeur : (char)20. |
| static constexpr [FieldStartChar](./fieldstartchar/) | Caractère de début de champ MS Word : (char)19. |
| static constexpr [LineBreakChar](./linebreakchar/) | Caractère de saut de ligne : (char)11 ou "\v". |
| static constexpr [LineFeedChar](./linefeedchar/) | Caractère de saut de ligne : (char)10 ou "\n". |
| static constexpr [NonBreakingHyphenChar](./nonbreakinghyphenchar/) | Le trait d'union insécable dans Microsoft Word est (char)30. |
| static constexpr [NonBreakingSpaceChar](./nonbreakingspacechar/) | Caractère d'espace insécable : (char)160. |
| static constexpr [OptionalHyphenChar](./optionalhyphenchar/) | Le trait d'union optionnel dans Microsoft Word est (char)31. |
| static constexpr [PageBreakChar](./pagebreakchar/) | Caractère de saut de page : (char)12 ou "\f". |
| static constexpr [ParagraphBreakChar](./paragraphbreakchar/) | Caractère de fin de paragraphe : (char)13 ou "\r". |
| static constexpr [SectionBreakChar](./sectionbreakchar/) | Caractère de fin de section : (char)12 ou "\f". |
| static constexpr [SpaceChar](./spacechar/) | Caractère d'espace : (char)32. |
| static constexpr [TabChar](./tabchar/) | Caractère de tabulation : (char)9 ou "\t". |

## Exemples



Montre comment utiliser les caractères de contrôle.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer des paragraphes avec du texte à l'aide de DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// La conversion du document en texte révèle que les caractères de contrôle
// représentent certains des éléments structurels du document, tels que les sauts de page.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Lors de la conversion d'un document en chaîne de caractères,
// nous pouvons omettre certains caractères de contrôle avec la méthode Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
