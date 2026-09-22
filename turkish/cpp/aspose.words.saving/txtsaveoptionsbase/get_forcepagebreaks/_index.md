---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks yöntemi"
linktitle: "get_ForcePageBreaks"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks yöntemi. Sayfa sonlarının dışa aktarım sırasında korunup korunmayacağını belirtmeye olanak tanır. Varsayılan değer C++'da false'tur."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


Dışa aktarım sırasında sayfa sonlarının korunup korunmayacağını belirtmeye olanak tanır. Varsayılan değer **false**'dur.

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## Örnekler



Bir belgeyi düz metne dışa aktarırken sayfa sonlarının korunup korunmayacağını nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3");

// Bir "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" metoduna geçirebiliriz.
// belgeyi düz metne kaydetme şeklimizi değiştirmek için yöntem.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Aspose.Words "Document" nesneleri, Microsoft Word belgeleri gibi sayfa sonlarına sahiptir.
// ".txt" gibi kaydetme formatları, sayfa sonları olmadan tek bir sürekli metin bloğudur.
// "ForcePageBreaks" özelliğini "true" olarak ayarlayın, tüm sayfa sonlarını '\f' karakterleri şeklinde korumak için.
// "ForcePageBreaks" özelliğini "false" olarak ayarlayın, tüm sayfa sonlarını atmak için.
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// Sayfa sonları içeren bir düz metin belgesi yüklerseniz,
// "Document" nesnesi bunları gövdeyi sayfalara bölmek için kullanacaktır.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## Ayrıca Bakınız

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
