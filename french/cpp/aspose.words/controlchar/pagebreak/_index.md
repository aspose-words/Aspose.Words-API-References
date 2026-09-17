---
title: "Méthode Aspose::Words::ControlChar::PageBreak"
linktitle: "PageBreak"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ControlChar::PageBreak. Caractère de saut de page : \"\\x000c\" ou \"\\f\". Notez qu'il a la même valeur que SectionBreak en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/controlchar/pagebreak/
---
## ControlChar::PageBreak method


Caractère de saut de page : "\x000c" ou "\f". Notez qu'il a la même valeur que [SectionBreak](../sectionbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::PageBreak()
```


## Exemples



Montre comment ajouter divers caractères de contrôle à un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajouter un espace normal.
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::SpaceChar + u"After space.");

// Ajouter un NBSP, qui est un espace insécable.
// Contrairement à l'espace normal, cet espace ne peut pas avoir de saut de ligne automatique à sa position.
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::NonBreakingSpace() + u"After space.");

// Ajouter un caractère de tabulation.
builder->Write(System::String(u"Before tab.") + Aspose::Words::ControlChar::Tab() + u"After tab.");

// Ajouter un saut de ligne.
builder->Write(System::String(u"Before line break.") + Aspose::Words::ControlChar::LineBreak() + u"After line break.");

// Ajouter une nouvelle ligne et commencer un nouveau paragraphe.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());
builder->Write(System::String(u"Before line feed.") + Aspose::Words::ControlChar::LineFeed() + u"After line feed.");
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// Le caractère de saut de ligne possède deux versions.
ASSERT_EQ(Aspose::Words::ControlChar::LineFeed(), Aspose::Words::ControlChar::Lf());

// Les retours chariot et les sauts de ligne peuvent être représentés ensemble par un seul caractère.
ASSERT_EQ(Aspose::Words::ControlChar::CrLf(), Aspose::Words::ControlChar::Cr() + Aspose::Words::ControlChar::Lf());

// Ajouter un saut de paragraphe, qui commencera un nouveau paragraphe.
builder->Write(System::String(u"Before paragraph break.") + Aspose::Words::ControlChar::ParagraphBreak() + u"After paragraph break.");
ASSERT_EQ(3, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// Ajouter un saut de section. Cela ne crée pas une nouvelle section ou un nouveau paragraphe.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
builder->Write(System::String(u"Before section break.") + Aspose::Words::ControlChar::SectionBreak() + u"After section break.");
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Ajouter un saut de page.
builder->Write(System::String(u"Before page break.") + Aspose::Words::ControlChar::PageBreak() + u"After page break.");

// Un saut de page a la même valeur qu'un saut de section.
ASSERT_EQ(Aspose::Words::ControlChar::PageBreak(), Aspose::Words::ControlChar::SectionBreak());

// Insérer une nouvelle section, puis définir son nombre de colonnes à deux.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc));
builder->MoveToSection(1);
builder->get_CurrentSection()->get_PageSetup()->get_TextColumns()->SetCount(2);

// Nous pouvons utiliser un caractère de contrôle pour marquer le point où le texte passe à la colonne suivante.
builder->Write(System::String(u"Text at end of column 1.") + Aspose::Words::ControlChar::ColumnBreak() + u"Text at beginning of column 2.");

doc->Save(get_ArtifactsDir() + u"ControlChar.InsertControlChars.docx");

// Il existe des équivalents char et string pour la plupart des caractères.
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Cell()), Aspose::Words::ControlChar::CellChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::NonBreakingSpace()), Aspose::Words::ControlChar::NonBreakingSpaceChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Tab()), Aspose::Words::ControlChar::TabChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineBreak()), Aspose::Words::ControlChar::LineBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineFeed()), Aspose::Words::ControlChar::LineFeedChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ParagraphBreak()), Aspose::Words::ControlChar::ParagraphBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::SectionBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::PageBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ColumnBreak()), Aspose::Words::ControlChar::ColumnBreakChar);
```

## Voir aussi

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
