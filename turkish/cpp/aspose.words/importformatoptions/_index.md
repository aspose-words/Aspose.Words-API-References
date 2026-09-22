---
title: "Aspose::Words::ImportFormatOptions sınıfı"
linktitle: "ImportFormatOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions sınıfı. Çıktıyı biçimlendirmek için çeşitli içe aktarma seçeneklerini belirtmenizi sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 35000
url: /tr/cpp/aspose.words/importformatoptions/
---
## ImportFormatOptions class


Çıktıyı biçimlendirmek için çeşitli içe aktarma seçeneklerini belirtmeye olanak tanır. Daha fazla bilgi edinmek için [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) dokümantasyon makalesini ziyaret edin.

```cpp
class ImportFormatOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/)() const | Cümle ve kelime aralığını otomatik olarak ayarlayıp ayarlamayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**. |
| [get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/)() const | İlk içe aktarılan bölüm tipini, [NewPage](../sectionstart/) olarak zorla değiştireceğini belirten bir boolean değer alır veya ayarlar; [AppendDocument()](../) çağrıldığında. Varsayılan değer **true**. |
| [get_ForceCopyStyles](./get_forcecopystyles/)() const | Çakışan stilleri [KeepSourceFormatting](../importformatmode/) modunda kopyalayıp kopyalamayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**. |
| [get_IgnoreHeaderFooter](./get_ignoreheaderfooter/)() const | [KeepSourceFormatting](../importformatmode/) modu kullanıldığında başlık/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **true**. |
| [get_IgnoreTextBoxes](./get_ignoretextboxes/)() const | [KeepSourceFormatting](../importformatmode/) modu kullanıldığında metin kutularının içerik kaynak biçimlendirmesinin yoksayılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **true**. |
| [get_KeepSourceNumbering](./get_keepsourcenumbering/)() const | Kaynak ve hedef belgelerde numaralandırma çakıştığında nasıl içe aktarılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**. |
| [get_MergePastedLists](./get_mergepastedlists/)() const | Yapıştırılan listelerin çevredeki listelerle birleştirileceğini belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**. |
| [get_ResolveThemeColors](./get_resolvethemecolors/)() const | Şekillerin tema renklerini zorla çözümleyeceğini belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**. |
| [get_SmartStyleBehavior](./get_smartstylebehavior/)() const | Kaynak ve hedef belgelerde aynı ada sahip stillerin nasıl içe aktarılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**. |
| [GetType](./gettype/)() const override |  |
| [ImportFormatOptions](./importformatoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AdjustSentenceAndWordSpacing](./set_adjustsentenceandwordspacing/)(bool) | [Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/) için ayarlayıcı. |
| [set_AppendDocumentWithNewPage](./set_appenddocumentwithnewpage/)(bool) | [Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/) için ayarlayıcı. |
| [set_ForceCopyStyles](./set_forcecopystyles/)(bool) | [Aspose::Words::ImportFormatOptions::get_ForceCopyStyles](./get_forcecopystyles/) için ayarlayıcı. |
| [set_IgnoreHeaderFooter](./set_ignoreheaderfooter/)(bool) | [Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter](./get_ignoreheaderfooter/) için ayarlayıcı. |
| [set_IgnoreTextBoxes](./set_ignoretextboxes/)(bool) | [Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes](./get_ignoretextboxes/) için ayarlayıcı. |
| [set_KeepSourceNumbering](./set_keepsourcenumbering/)(bool) | [Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering](./get_keepsourcenumbering/) için ayarlayıcı. |
| [set_MergePastedLists](./set_mergepastedlists/)(bool) | [Aspose::Words::ImportFormatOptions::get_MergePastedLists](./get_mergepastedlists/) için ayarlayıcı. |
| [set_ResolveThemeColors](./set_resolvethemecolors/)(bool) | [Aspose::Words::ImportFormatOptions::get_ResolveThemeColors](./get_resolvethemecolors/) için ayarlayıcı. |
| [set_SmartStyleBehavior](./set_smartstylebehavior/)(bool) | Ayarlayıcı için [Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior](./get_smartstylebehavior/). |
| static [Type](./type/)() |  |

## Örnekler



Belgeleri eklerken yinelenen stilleri nasıl çözeceğini gösterir.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Belgeyi klonlayın ve klonun "MyStyle" stilini düzenleyin, böylece orijinalinkinden farklı bir renge sahip olur.
// Klonu orijinal belgeye eklerseniz, aynı ada sahip iki stil çakışmaya neden olur.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// SmartStyleBehavior'ı etkinleştirdiğimizde ve KeepSourceFormatting içe aktarma biçim modunu kullandığımızda,
// Aspose.Words, kaynak belge stillerini dönüştürerek stil çakışmalarını çözecektir.
// hedef stillerle aynı isimlere sahip olanları doğrudan paragraf özniteliklerine dönüştürerek.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
