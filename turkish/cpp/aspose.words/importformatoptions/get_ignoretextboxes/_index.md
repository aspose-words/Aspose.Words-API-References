---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes yöntemi"
linktitle: "get_IgnoreTextBoxes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes yöntemi. KeepSourceFormatting modu kullanıldığında metin kutularının içeriğinin kaynak biçimlendirmesinin yoksayılacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'ta true'dur."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/importformatoptions/get_ignoretextboxes/
---
## ImportFormatOptions::get_IgnoreTextBoxes method


Metin kutularının içeriğinin kaynak biçimlendirmesinin yoksayılacağını belirten bir boolean değer alır veya ayarlar, eğer [KeepSourceFormatting](../../importformatmode/) modu kullanılıyorsa. Varsayılan değer **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes() const
```


## Örnekler



Bir belge eklenirken metin kutusu biçimlendirmesinin nasıl yönetileceğini gösterir.
```cpp
// Başka bir belgeden düğümler eklenmiş bir belge oluşturun.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

builder->Writeln(u"Hello world!");

// İlk belgeye aktaracağımız bir metin kutusu içeren başka bir belge oluşturun.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 100);
builder->MoveTo(textBox->get_FirstParagraph());
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Name(u"Courier New");
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Size(24);
builder->Write(u"Textbox contents");

// Metin kutusu biçimlendirmesini temizlemek mi yoksa korumak mı istediğinizi belirten bir bayrak ayarlayın
// diğer belgelere aktarırken.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreTextBoxes(ignoreTextBoxes);

// Metin kutusunu kaynak belgeden hedef belgeye aktarın,
// ve ardından metin içeriğinin stilini koruyup korumadığımızı doğrulayın.
auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);
auto importedTextBox = System::ExplicitCast<Aspose::Words::Drawing::Shape>(importer->ImportNode(textBox, true));
dstDoc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedTextBox);

if (ignoreTextBoxes)
{
    ASPOSE_ASSERT_EQ(12.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Times New Roman", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}
else
{
    ASPOSE_ASSERT_EQ(24.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Courier New", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.IgnoreTextBoxes.docx");
```

## Ayrıca Bakınız

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
