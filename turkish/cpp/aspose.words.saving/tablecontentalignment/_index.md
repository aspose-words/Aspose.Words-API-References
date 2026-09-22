---
title: "Aspose::Words::Saving::TableContentAlignment enum"
linktitle: "TableContentAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TableContentAlignment enum. C++'ta Markdown formatına dışa aktarılırken kullanılacak tablo içeriğinin hizalamasını belirtmeye olanak tanır."
type: docs
weight: 84000
url: /tr/cpp/aspose.words.saving/tablecontentalignment/
---
## TableContentAlignment enum


Markdown formatına dışa aktarılırken kullanılacak tablonun içeriğinin hizalamasını belirtmeye olanak tanır.

```cpp
enum class TableContentAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Otomatik | 0 | Hizalama, ilgili tablo sütunundaki ilk paragraftan alınacaktır. |
| Sol | 1 | Tabloların içeriği sola hizalanacaktır. |
| Orta | 2 | Tabloların içeriği ortaya hizalanacaktır. |
| Sağ | 3 | Tabloların içeriği sağa hizalanacaktır. |


## Örnekler



Tablolardaki içeriklerin nasıl hizalanacağını gösterir.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_TableContentAlignment(tableContentAlignment);

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

switch (tableContentAlignment)
{
    case Aspose::Words::Saving::TableContentAlignment::Auto:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

    case Aspose::Words::Saving::TableContentAlignment::Left:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

    case Aspose::Words::Saving::TableContentAlignment::Center:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

    case Aspose::Words::Saving::TableContentAlignment::Right:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
