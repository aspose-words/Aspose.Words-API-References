---
title: "Aspose::Words::LineNumberRestartMode enum"
linktitle: "LineNumberRestartMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LineNumberRestartMode enum. Otomatik satır numaralandırmanın C++'ta ne zaman yeniden başlayacağını belirler."
type: docs
weight: 94000
url: /tr/cpp/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enum


Otomatik satır numaralandırmasının ne zaman yeniden başlayacağını belirler.

```cpp
enum class LineNumberRestartMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| RestartPage | 0 | Satır numaralandırma her sayfanın başında yeniden başlar. |
| RestartSection | 1 | Satır numaralandırma bölümün başlangıcında yeniden başlar. |
| Continuous | 2 | Satır numaralandırma önceki bölümden devam eder. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
