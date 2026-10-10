---
title: "Aspose::Words::Bibliography::ContributorCollection 类"
linktitle: "贡献者集合"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Bibliography::ContributorCollection 类。表示 C++ 中的书目来源贡献者。"
type: docs
weight: 375
url: /zh/cpp/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class


表示参考文献来源的贡献者。

```cpp
class ContributorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bibliography::Contributor>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Artist](./get_artist/)() | 获取或设置来源的艺术家。 |
| [get_Author](./get_author/)() | 获取或设置来源的作者。 |
| [get_BookAuthor](./get_bookauthor/)() | 获取或设置来源的图书作者。 |
| [get_Compiler](./get_compiler/)() | 获取或设置来源的编译者。 |
| [get_Composer](./get_composer/)() | 获取或设置来源的作曲者。 |
| [get_Conductor](./get_conductor/)() | 获取或设置来源的指挥。 |
| [get_Counsel](./get_counsel/)() | 获取或设置来源的顾问。 |
| [get_Director](./get_director/)() | 获取或设置来源的导演。 |
| [get_Editor](./get_editor/)() | 获取或设置来源的编辑。 |
| [get_Interviewee](./get_interviewee/)() | 获取或设置来源的受访者。 |
| [get_Interviewer](./get_interviewer/)() | 获取或设置来源的采访者。 |
| [get_Inventor](./get_inventor/)() | 获取或设置来源的发明者。 |
| [get_Performer](./get_performer/)() | 获取或设置来源的表演者。 |
| [get_Producer](./get_producer/)() | 获取或设置来源的制片人。 |
| [get_Translator](./get_translator/)() | 获取或设置来源的译者。 |
| [get_Writer](./get_writer/)() | 获取或设置来源的作者。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Artist](./set_artist/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Artist](./get_artist/) 的设置器。 |
| [set_Author](./set_author/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Author](./get_author/) 的设置器。 |
| [set_BookAuthor](./set_bookauthor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_BookAuthor](./get_bookauthor/) 的设置器。 |
| [set_Compiler](./set_compiler/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Compiler](./get_compiler/) 的设置器。 |
| [set_Composer](./set_composer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Composer](./get_composer/) 的设置器。 |
| [set_Conductor](./set_conductor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Conductor](./get_conductor/) 的设置器。 |
| [set_Counsel](./set_counsel/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Counsel](./get_counsel/) 的设置器。 |
| [set_Director](./set_director/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Director](./get_director/) 的设置器。 |
| [set_Editor](./set_editor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Editor](./get_editor/) 的设置器。 |
| [set_Interviewee](./set_interviewee/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Interviewee](./get_interviewee/) 的设置器。 |
| [set_Interviewer](./set_interviewer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Interviewer](./get_interviewer/) 的设置器。 |
| [set_Inventor](./set_inventor/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Inventor](./get_inventor/) 的设置器。 |
| [set_Performer](./set_performer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Performer](./get_performer/) 的设置器。 |
| [set_Producer](./set_producer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Producer](./get_producer/) 的设置器。 |
| [set_Translator](./set_translator/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Translator](./get_translator/) 的设置器。 |
| [set_Writer](./set_writer/)(const System::SharedPtr\<Aspose::Words::Bibliography::Contributor\>\&) | 用于 [Aspose::Words::Bibliography::ContributorCollection::get_Writer](./get_writer/) 的设置器。 |
| static [Type](./type/)() |  |

## 示例



展示如何获取文档中可用的书目来源。
```cpp
auto document = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bibliography sources.docx");

System::SharedPtr<Aspose::Words::Bibliography::Bibliography> bibliography = document->get_Bibliography();
ASSERT_EQ(12, bibliography->get_Sources()->get_Count());

// 从书目来源获取默认数据。
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

// 此外，您可以创建一个新来源。
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

## 另见

* Namespace [Aspose::Words::Bibliography](../)
* Library [Aspose.Words for C++](../../)
