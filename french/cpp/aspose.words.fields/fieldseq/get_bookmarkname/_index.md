---
title: "Méthode Aspose::Words::Fields::FieldSeq::get_BookmarkName"
linktitle: "get_BookmarkName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldSeq::get_BookmarkName. Obtient ou définit le nom d'un signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


Obtient ou définit le nom d'un signet qui fait référence à un élément ailleurs dans le document plutôt qu'à l'emplacement actuel.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## Exemples



Montre comment combiner la table des matières et les champs de séquence.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ trouvé dans le document.
// Chaque entrée contient le paragraphe qui contient le champ SEQ,
// et le numéro de la page où le champ apparaît.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Configurez ce champ TOC pour qu'il possède une propriété SequenceIdentifier avec la valeur "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Configurez ce champ TOC pour ne récupérer que les champs SEQ qui se trouvent à l'intérieur des limites d'un signet
// nommé "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
// Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique.
// identifié par la propriété "SequenceIdentifier" du champ SEQ.
// Insérez un champ SEQ dont l'identifiant de séquence correspond à celui du TOC
// propriété TableOfFiguresLabel. Ce champ ne créera pas d'entrée dans le TOC car il se trouve en dehors
// des limites du signet désignées par "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// La séquence de ce champ SEQ correspond à la propriété "TableOfFiguresLabel" du TOC et se trouve à l'intérieur des limites du signet.
// Le paragraphe contenant ce champ apparaîtra dans le TOC en tant qu'entrée.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// La séquence de ce champ SEQ ne correspond pas à la propriété "TableOfFiguresLabel" du TOC,
// et se trouve à l'intérieur des limites du signet. Son paragraphe n'apparaîtra pas dans le TOC en tant qu'entrée.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// La séquence de ce champ SEQ correspond à la propriété "TableOfFiguresLabel" du TOC et se trouve à l'intérieur des limites du signet.
// Ce champ fait également référence à un autre signet. Le contenu de ce signet apparaîtra dans l'entrée du TOC pour ce champ SEQ.
// Le champ SEQ lui‑même n'affichera pas le contenu de ce signet.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Créez un signet avec un contenu qui apparaîtra dans l'entrée du TOC en raison du champ SEQ ci‑dessus qui le référence.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## Voir aussi

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
