---
title: "Aspose::Words::Bibliography::PersonCollection classe"
linktitle: "PersonCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Bibliography::PersonCollection classe. Rappresenta un elenco di persone che sono contributori della fonte bibliografica in C++."
type: docs
weight: 750
url: /it/cpp/aspose.words.bibliography/personcollection/
---
## PersonCollection class


Rappresenta un elenco di persone che sono contributori di fonti bibliografiche.

```cpp
class PersonCollection : public Aspose::Words::Bibliography::Contributor,
                         public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bibliography::Person>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\&) | Aggiunge un [Person](../person/) alla collezione. |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [Contains](./contains/)(const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\&) | Determina se la collezione contiene una persona specifica. |
| [get_Count](./get_count/)() | Ottiene il numero di persone contenute nella collezione. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta una persona all'indice specificato. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\&) | Ottiene o imposta una persona all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PersonCollection](./personcollection/)() | Inizializza una nuova istanza della classe [PersonCollection](./). |
| [PersonCollection](./personcollection/)(const System::SharedPtr\<System::Collections::Generic::IEnumerable\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\>\&) |  |
| [PersonCollection](./personcollection/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\&) | Inizializza una nuova istanza della classe [PersonCollection](./). |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\&) | Rimuove la persona dalla collezione. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove la persona all'indice specificato. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come ottenere le fonti bibliografiche disponibili nel documento.
```cpp
auto document = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bibliography sources.docx");

System::SharedPtr<Aspose::Words::Bibliography::Bibliography> bibliography = document->get_Bibliography();
ASSERT_EQ(12, bibliography->get_Sources()->get_Count());

// Ottieni i dati predefiniti dalle fonti bibliografiche.
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

// Inoltre, è possibile creare una nuova fonte.
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

## Vedi anche

* Class [Contributor](../contributor/)
* Namespace [Aspose::Words::Bibliography](../)
* Library [Aspose.Words for C++](../../)
