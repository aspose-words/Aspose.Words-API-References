---
title: "Aspose::Words::Node::ToString metodu"
linktitle: "ToString"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::ToString metodu. Düğümün içeriğini belirtilen formatta bir dizeye C++'ta dışa aktarır."
type: docs
weight: 22000
url: /tr/cpp/aspose.words/node/tostring/
---
## Node::ToString(Aspose::Words::SaveFormat) method


Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır.

```cpp
System::String Aspose::Words::Node::ToString(Aspose::Words::SaveFormat saveFormat)
```


### ReturnValue

Belirtilen formatta düğümün içeriği.

## Örnekler



Bir düğümde GetText ve ToString metodlarını çağırma arasındaki farkı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText, görünen metni ve alan kodlarını ayrıca özel karakterleri alacaktır.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString, belgeyi belirtilen kaydetme formatına kaydedildiğinde görünümünü verir.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


Liste öğesi olan tüm paragrafların liste etiketlerini nasıl çıkaracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Paragraf listesinin olup olmadığını bulun. Belgemizde, listemiz sade Arap rakamları kullanıyor,
// ki üçten başlayıp altıya kadar devam eder.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // Bu, bu düğümü metin biçiminde çıktıya aldığımızda elde ettiğimiz metindir.
    // Bu metin çıktısı liste etiketlerini atlayacaktır. Herhangi bir paragraf biçimlendirme karakterini temizleyin.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // Bu, paragrafın listedeki mevcut seviyedeki konumunu alır. Birden fazla seviyeye sahip bir listemiz varsa,
    // bu, o seviyedeki konumunu bize söyleyecektir.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // Çıktıda metinle birlikte liste etiketini eklemek için bunları birleştirin.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```


Bir düğümün içeriğini HTML formatında String'e dışa aktarır.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// html SaveFormat aşırı yüklemesiyle ToString metodunu çağırdığımızda,
// düğümün içeriğini ham html temsiline dönüştürür.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Bu dönüşümün sonucunu bir SaveOptions nesnesi kullanarak da değiştirebiliriz.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## Ayrıca Bakınız

* Enum [SaveFormat](../../saveformat/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Node::ToString(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır.

```cpp
System::String Aspose::Words::Node::ToString(const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Düğümün nasıl kaydedileceğini kontrol eden seçenekleri belirler. |

### ReturnValue

Belirtilen formatta düğümün içeriği.

## Örnekler



Bir düğümün içeriğini HTML formatında String'e dışa aktarır.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// html SaveFormat aşırı yüklemesiyle ToString metodunu çağırdığımızda,
// düğümün içeriğini ham html temsiline dönüştürür.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Bu dönüşümün sonucunu bir SaveOptions nesnesi kullanarak da değiştirebiliriz.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## Ayrıca Bakınız

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
