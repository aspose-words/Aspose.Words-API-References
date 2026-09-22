---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak yöntemi"
linktitle: "get_ParagraphBreak"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak yöntemi. C++'ta metin formatlarında dışa aktarırken paragraf sonu olarak kullanılacak dizeyi belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/txtsaveoptionsbase/get_paragraphbreak/
---
## TxtSaveOptionsBase::get_ParagraphBreak method


Metin formatlarında dışa aktarırken paragraf sonu olarak kullanılacak dizeyi belirtir.

```cpp
System::String Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak() const
```

## Açıklamalar


Varsayılan değer [CrLf](../../../aspose.words/controlchar/crlf/)dir.

## Örnekler



Özel bir paragraf sonu ile .txt belgesinin nasıl kaydedileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Bir "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" yöntemine aktarabiliriz
// belgeyi düz metne kaydetme şeklini değiştirmek için.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// "ParagraphBreak" özelliğini her paragrafın sonuna koymak istediğimiz özel bir değere ayarlayın.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## Ayrıca Bakınız

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
