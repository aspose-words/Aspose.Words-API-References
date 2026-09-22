---
title: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method"
linktitle: "get_AddBidiMarks"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks yöntemi. Düz metin formatında dışa aktarırken her BiDi çalıştırmadan önce çift yönlü işaretler eklenip eklenmeyeceğini belirtir. Varsayılan değer C++'ta false'tur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/txtsaveoptions/get_addbidimarks/
---
## TxtSaveOptions::get_AddBidiMarks method


Düz metin formatında dışa aktarırken her BiDi çalışmasından önce çift yönlü işaretler eklenip eklenmeyeceğini belirtir. Varsayılan değer **false**'dır.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks() const
```


## Örnekler



Metindeki her çift yönlü [Run](../../../aspose.words/run/) öncesine Unicode Karakteri 'RIGHT-TO-LEFT MARK' (U+200F) eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Bidi(true);
builder->Writeln(u"שלום עולם!");
builder->Writeln(u"مرحبا بالعالم!");

// Bir "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" yöntemine aktarabiliriz
// belgeyi düz metne kaydetme şeklini değiştirmek için.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_Encoding(System::Text::Encoding::get_Unicode());

// Çalıştırmalardan önce işaret eklemek için "AddBidiMarks" özelliğini "true" olarak ayarlayın
// sağdan sola metinle bu durumu belirtmek için.
// Tüm soldan sağa yazmak için "AddBidiMarks" özelliğini "false" olarak ayarlayın
// ve sağdan sola çalıştırmayı da aynı şekilde, hangisinin hangisi olduğunu belirten bir şey olmadan yazın.
saveOptions->set_AddBidiMarks(addBidiMarks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt", saveOptions);

System::String docText = System::Text::Encoding::get_Unicode()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    ASSERT_EQ(u"\ufeffHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    ASSERT_TRUE(docText.Contains(u"\u200f"));
}
else
{
    ASSERT_EQ(u"\ufeffHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    ASSERT_FALSE(docText.Contains(u"\u200f"));
}
```

## Ayrıca Bakınız

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
