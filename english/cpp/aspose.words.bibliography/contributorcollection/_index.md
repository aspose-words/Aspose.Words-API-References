---
title: Aspose::Words::Bibliography::ContributorCollection class
linktitle: ContributorCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Bibliography::ContributorCollection class. Represents bibliography source contributors in C++.'
type: docs
weight: 375
url: /cpp/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class


Represents bibliography source contributors.

```cpp
class ContributorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bibliography::Contributor>>
```

## Methods

| Method | Description |
| --- | --- |
| [get_Artist](./get_artist/)() | Gets or sets the artist of a source. |
| [get_Author](./get_author/)() | Gets or sets the author of a source. |
| [get_BookAuthor](./get_bookauthor/)() | Gets or sets the book author of a source. |
| [get_Compiler](./get_compiler/)() | Gets or sets the compiler of a source. |
| [get_Composer](./get_composer/)() | Gets or sets the composer of a source. |
| [get_Conductor](./get_conductor/)() | Gets or sets the conductor of a source. |
| [get_Counsel](./get_counsel/)() | Gets or sets the counsel of a source. |
| [get_Director](./get_director/)() | Gets or sets the director of a source. |
| [get_Editor](./get_editor/)() | Gets or sets the editor of a source. |
| [get_Interviewee](./get_interviewee/)() | Gets or sets the interviewee of a source. |
| [get_Interviewer](./get_interviewer/)() | Gets or sets the interviewer of a source. |
| [get_Inventor](./get_inventor/)() | Gets or sets the inventor of a source. |
| [get_Performer](./get_performer/)() | Gets or sets the performer of a source. |
| [get_Producer](./get_producer/)() | Gets or sets the producer of a source. |
| [get_Translator](./get_translator/)() | Gets or sets the translator of a source. |
| [get_Writer](./get_writer/)() | Gets or sets the writer of a source. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Artist](./set_artist/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Artist](./get_artist/). |
| [set_Author](./set_author/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Author](./get_author/). |
| [set_BookAuthor](./set_bookauthor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_BookAuthor](./get_bookauthor/). |
| [set_Compiler](./set_compiler/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Compiler](./get_compiler/). |
| [set_Composer](./set_composer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Composer](./get_composer/). |
| [set_Conductor](./set_conductor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Conductor](./get_conductor/). |
| [set_Counsel](./set_counsel/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Counsel](./get_counsel/). |
| [set_Director](./set_director/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Director](./get_director/). |
| [set_Editor](./set_editor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Editor](./get_editor/). |
| [set_Interviewee](./set_interviewee/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Interviewee](./get_interviewee/). |
| [set_Interviewer](./set_interviewer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Interviewer](./get_interviewer/). |
| [set_Inventor](./set_inventor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Inventor](./get_inventor/). |
| [set_Performer](./set_performer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Performer](./get_performer/). |
| [set_Producer](./set_producer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Producer](./get_producer/). |
| [set_Translator](./set_translator/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Translator](./get_translator/). |
| [set_Writer](./set_writer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | Setter for [Aspose::Words::Bibliography::ContributorCollection::get_Writer](./get_writer/). |
| static [Type](./type/)() |  |

## Examples



Shows how to get bibliography sources available in the document. 
```cpp
auto document = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bibliography sources.docx");

System::SharedPtr<Aspose::Words::Bibliography::Bibliography> bibliography = document->get_Bibliography();
ASSERT_EQ(12, bibliography->get_Sources()->get_Count());

// Get default data from bibliography sources.
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

// Also, you can create a new source.
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

## See Also

* Namespace [Aspose::Words::Bibliography](../)
* Library [Aspose.Words for C++](../../)
