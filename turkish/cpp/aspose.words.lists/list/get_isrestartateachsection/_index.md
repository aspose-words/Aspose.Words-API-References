---
title: "Aspose::Words::Lists::List::get_IsRestartAtEachSection metodu"
linktitle: "get_IsRestartAtEachSection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::List::get_IsRestartAtEachSection metodu. Listenin her bölümde yeniden başlatılıp başlatılmayacağını belirtir. Varsayılan değer C++'ta false'tur."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


Listenin her bölümde yeniden başlatılıp başlatılmayacağını belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## Açıklamalar


Bu seçenek yalnızca RTF, DOC ve DOCX belge formatlarında desteklenir.

Bu seçenek, [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/) değerinden daha yüksek olduğunda yalnızca DOCX'e yazılacaktır.

## Örnekler



Bir listedeki numaralandırmanın her bölümde yeniden başlamasını nasıl yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// \"IsRestartAtEachSection\" özelliği yalnızca şu durumda uygulanabilir:
// belgenin OOXML uyumluluk seviyesi \"OoxmlComplianceCore.Ecma376\"'den daha yeni bir standarda ayarlandığında.
auto options = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
options->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```

## Ayrıca Bakınız

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
