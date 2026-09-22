---
title: "Aspose::Words::PageSetup::get_LineNumberCountBy yöntemi"
linktitle: "get_LineNumberCountBy"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_LineNumberCountBy yöntemi. Satır numaraları için sayısal artışı döndürür veya ayarlar C++'ta."
type: docs
weight: 23000
url: /tr/cpp/aspose.words/pagesetup/get_linenumbercountby/
---
## PageSetup::get_LineNumberCountBy method


Satır numaraları için sayısal artışı alır veya ayarlar.

```cpp
int32_t Aspose::Words::PageSetup::get_LineNumberCountBy()
```


## Örnekler



Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bölümün PageSetup nesnesini kullanarak sayıları bölümün metin satırlarının solunda gösterebiliriz.
// Bu, bir List nesnesiyle aynı davranıştır,
// ancak tüm bölümü kapsar ve metni hiçbir şekilde değiştirmez.
// Bölümümüz her yeni sayfada numaralandırmayı 1'den yeniden başlatacak ve sayıyı gösterecek,
// eğer 3'ün katıysa, satırın solunda 50pt konumda.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_LineStartingNumber(1);
pageSetup->set_LineNumberCountBy(3);
pageSetup->set_LineNumberRestartMode(Aspose::Words::LineNumberRestartMode::RestartPage);
pageSetup->set_LineNumberDistanceFromText(50.0);

for (int32_t i = 1; i <= 25; i++)
{
    builder->Writeln(System::String::Format(u"Line {0}.", i));
}

// Satır sayacı, "SuppressLineNumbers" bayrağı "true" olarak ayarlanmış herhangi bir paragrafı atlayacaktır.
// Bu paragraf 15. satırda, ki bu 3'ün katıdır ve bu yüzden normalde bir satır numarası gösterirdi.
// Bölümün satır sayacı da bu satırı yok sayacak, bir sonraki satırı 15. olarak ele alacak,
// ve sayımı o noktadan itibaren devam ettirecek.
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(14)->get_ParagraphFormat()->set_SuppressLineNumbers(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.LineNumbers.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
