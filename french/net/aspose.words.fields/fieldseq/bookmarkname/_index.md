---
title: FieldSeq.BookmarkName
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldSeq propriété. Obtient ou définit un nom de signet qui fait référence à un élément ailleurs dans le document plutôt quà lemplacement actuel.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Obtient ou définit un nom de signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel.

```csharp
public string BookmarkName { get; set; }
```

### Exemples

Montre comment combiner la table des matières et les champs de séquence.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ présent dans le document.
// Chaque entrée contient le paragraphe qui contient le champ SEQ,
// et le numéro de la page sur laquelle le champ apparaît.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Configurez ce champ TOC pour avoir une propriété SequenceIdentifier avec une valeur de "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Configurez ce champ TOC pour ne récupérer que les champs SEQ qui se trouvent dans les limites d'un signet
// nommé "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// Les champs SEQ affichent un décompte qui s'incrémente à chaque champ SEQ.
// Ces champs conservent également des décomptes séparés pour chaque séquence nommée unique
// identifié par la propriété "SequenceIdentifier" du champ SEQ.
// Insère un champ SEQ qui a un identifiant de séquence qui correspond à la table des matières
// Propriété TableOfFiguresLabel. Ce champ ne créera pas d'entrée dans la table des matières puisqu'il se trouve à l'extérieur
// les limites du signet désignées par "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// La séquence de ce champ SEQ correspond à la propriété "TableOfFiguresLabel" de la table des matières et se trouve dans les limites du signet.
// Le paragraphe qui contient ce champ apparaîtra dans la table des matières en tant qu'entrée.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// La séquence de ce champ SEQ ne correspond pas à la propriété "TableOfFiguresLabel" de la table des matières,
// et est dans les limites du signet. Son paragraphe n'apparaîtra pas dans la table des matières en tant qu'entrée.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// La séquence de ce champ SEQ correspond à la propriété "TableOfFiguresLabel" de la table des matières et se situe dans les limites du signet.
// Ce champ fait également référence à un autre signet. Le contenu de ce signet apparaîtra dans l'entrée TOC pour ce champ SEQ.
// Le champ SEQ lui-même n'affichera pas le contenu de ce signet.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Crée un signet avec du contenu qui apparaîtra dans l'entrée TOC en raison du champ SEQ ci-dessus qui y fait référence.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

### Voir également

* class [FieldSeq](../)
* espace de noms [Aspose.Words.Fields](../../fieldseq/)
* Assemblée [Aspose.Words](../../../)


