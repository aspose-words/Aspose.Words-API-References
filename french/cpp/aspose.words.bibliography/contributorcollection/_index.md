---
title: "Aspose::Words::Bibliography::ContributorCollection class"
linktitle: "ContributorCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Bibliography::ContributorCollection class. Représente les contributeurs de sources bibliographiques en C++."
type: docs
weight: 375
url: /fr/cpp/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class


Représente les contributeurs à la source bibliographique.

```cpp
class ContributorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bibliography::Contributor>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Artist](./get_artist/)() | Obtient ou définit l'artiste d'une source. |
| [get_Author](./get_author/)() | Obtient ou définit l'auteur d'une source. |
| [get_BookAuthor](./get_bookauthor/)() | Obtient ou définit l'auteur du livre d'une source. |
| [get_Compiler](./get_compiler/)() | Obtient ou définit le compilateur d'une source. |
| [get_Composer](./get_composer/)() | Obtient ou définit le compositeur d'une source. |
| [get_Conductor](./get_conductor/)() | Obtient ou définit le chef d'orchestre d'une source. |
| [get_Counsel](./get_counsel/)() | Obtient ou définit le conseiller d'une source. |
| [get_Director](./get_director/)() | Obtient ou définit le directeur d'une source. |
| [get_Editor](./get_editor/)() | Obtient ou définit l'éditeur d'une source. |
| [get_Interviewee](./get_interviewee/)() | Obtient ou définit l'interviewé d'une source. |
| [get_Interviewer](./get_interviewer/)() | Obtient ou définit l'intervieweur d'une source. |
| [get_Inventor](./get_inventor/)() | Obtient ou définit l'inventeur d'une source. |
| [get_Performer](./get_performer/)() | Obtient ou définit l'interprète d'une source. |
| [get_Producer](./get_producer/)() | Obtient ou définit le producteur d'une source. |
| [get_Translator](./get_translator/)() | Obtient ou définit le traducteur d'une source. |
| [get_Writer](./get_writer/)() | Obtient ou définit l'écrivain d'une source. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Artist](./set_artist/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Mutateur pour [Aspose::Words::Bibliography::ContributorCollection::get_Artist](./get_artist/). |
| [set_Author](./set_author/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Author](./get_author/). |
| [set_BookAuthor](./set_bookauthor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_BookAuthor](./get_bookauthor/). |
| [set_Compiler](./set_compiler/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Compiler](./get_compiler/). |
| [set_Composer](./set_composer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Composer](./get_composer/). |
| [set_Conductor](./set_conductor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Conductor](./get_conductor/). |
| [set_Counsel](./set_counsel/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Counsel](./get_counsel/). |
| [set_Director](./set_director/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Director](./get_director/). |
| [set_Editor](./set_editor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Editor](./get_editor/). |
| [set_Interviewee](./set_interviewee/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Interviewee](./get_interviewee/). |
| [set_Interviewer](./set_interviewer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Interviewer](./get_interviewer/). |
| [set_Inventor](./set_inventor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Inventor](./get_inventor/). |
| [set_Performer](./set_performer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Performer](./get_performer/). |
| [set_Producer](./set_producer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Producer](./get_producer/). |
| [set_Translator](./set_translator/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Translator](./get_translator/). |
| [set_Writer](./set_writer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Définisseur pour [Aspose::Words::Bibliography::ContributorCollection::get_Writer](./get_writer/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment obtenir les sources bibliographiques disponibles dans le document.
```cpp
auto document = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bibliography sources.docx");

System::SharedPtr<Aspose::Words::Bibliography::Bibliography> bibliography = document->get_Bibliography();
ASSERT_EQ(12, bibliography->get_Sources()->get_Count());

// Obtenez les données par défaut des sources bibliographiques.
System::SharedPtr<Aspose::Words::Bibliography::Source> source = bibliography->get_Sources()->LINQ_FirstOrDefault();
ASSERT_EQ(u"Book 0 (No LCID)", source->get_Title());
ASSERT_EQ(Aspose::Words::Bibliography::SourceType::Book, source->get_SourceType());
ASSERT_EQ(3, source->get_Contributors()->LINQ_Count());
ASSERT_TRUE(System::TestTools::IsNull(source->get_AbbreviatedCaseNumber()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_AlbumTitle()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_BookTitle()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Broadcaster()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_BroadcastTitle()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_CaseNumber()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_ChapterNumber()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Comments()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_ConferenceName()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_CountryOrRegion()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Court()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Day()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_DayAccessed()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Department()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Distributor()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Doi()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Edition()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Guid()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Institution()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_InternetSiteTitle()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Issue()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_JournalName()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Lcid()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Medium()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Month()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_MonthAccessed()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_NumberVolumes()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Pages()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_PatentNumber()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_PeriodicalTitle()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_ProductionCompany()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_PublicationTitle()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Publisher()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_RecordingNumber()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_RefOrder()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Reporter()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_ShortTitle()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_StandardNumber()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_StateOrProvince()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Station()));
ASSERT_EQ(u"BookNoLCID", source->get_Tag());
ASSERT_TRUE(System::TestTools::IsNull(source->get_Theater()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_ThesisType()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Type()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Url()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Version()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Volume()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_Year()));
ASSERT_TRUE(System::TestTools::IsNull(source->get_YearAccessed()));

// De plus, vous pouvez créer une nouvelle source.
auto newSource = System::MakeObject<Aspose::Words::Bibliography::Source>(u"New source", Aspose::Words::Bibliography::SourceType::Misc);

System::SharedPtr<Aspose::Words::Bibliography::ContributorCollection> contributors = source->get_Contributors();
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Artist()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_BookAuthor()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Compiler()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Composer()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Conductor()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Counsel()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Director()));
ASSERT_FALSE(System::TestTools::IsNull(contributors->get_Editor()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Interviewee()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Interviewer()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Inventor()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Performer()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Producer()));
ASSERT_FALSE(System::TestTools::IsNull(contributors->get_Translator()));
ASSERT_TRUE(System::TestTools::IsNull(contributors->get_Writer()));

System::SharedPtr<Aspose::Words::Bibliography::Contributor> editor = contributors->get_Editor();
ASSERT_EQ(2, (System::ExplicitCast<Aspose::Words::Bibliography::PersonCollection>(editor))->LINQ_Count());

auto authors = System::ExplicitCast<Aspose::Words::Bibliography::PersonCollection>(contributors->get_Author());
ASSERT_EQ(2, authors->LINQ_Count());

System::SharedPtr<Aspose::Words::Bibliography::Person> person = authors->idx_get(0);
ASSERT_EQ(u"Roxanne", person->get_First());
ASSERT_EQ(u"Brielle", person->get_Middle());
ASSERT_EQ(u"Tejeda", person->get_Last());
```

## Voir aussi

* Namespace [Aspose::Words::Bibliography](../)
* Library [Aspose.Words for C++](../../)
