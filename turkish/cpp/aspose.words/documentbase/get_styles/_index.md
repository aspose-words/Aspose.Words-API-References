---
title: "Aspose::Words::DocumentBase::get_Styles yöntemi"
linktitle: "get_Styles"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBase::get_Styles yöntemi. Belge içinde tanımlanan stillerin bir koleksiyonunu döndürür C++'ta."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/documentbase/get_styles/
---
## DocumentBase::get_Styles method


Belgede tanımlı stillerin bir koleksiyonunu döndürür.

```cpp
System::SharedPtr<Aspose::Words::StyleCollection> Aspose::Words::DocumentBase::get_Styles() const
```

## Açıklamalar


Daha fazla bilgi için [StyleCollection](../../stylecollection/) sınıfının açıklamasına bakın.

## Örnekler



Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Aspose.Words kullanılarak oluşturulan bir belgenin varsayılan olarak içerdiği tüm stilleri numaralandırın ve listeleyin.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```


Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulup kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Özel bir paragraf stili oluştur.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Bir liste oluşturun ve bu stili kullanan paragrafların bu listeyi kullanmasını sağlayın.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Paragraf stilini belge oluşturucunun mevcut paragrafına uygulayın ve ardından metin ekleyin.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Belge oluşturucunun stilini liste biçimlendirmesi olmayan bir stile değiştirin ve başka bir paragraf yazın.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Ayrıca Bakınız

* Class [StyleCollection](../../stylecollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
