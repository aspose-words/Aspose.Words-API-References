---
title: "Aspose::Words::TextColumnCollection::get_LineBetween metodu"
linktitle: "get_LineBetween"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextColumnCollection::get_LineBetween metodu. true olduğunda, C++'da sütunlar arasında dikey bir çizgi ekler."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/textcolumncollection/get_linebetween/
---
## TextColumnCollection::get_LineBetween method


**true** olduğunda, sütunlar arasında dikey bir çizgi ekler.

```cpp
bool Aspose::Words::TextColumnCollection::get_LineBetween()
```


## Örnekler



Sütunları dikey bir çizgiyle nasıl ayıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Mevcut bölümün PageSetup nesnesini, metni birkaç sütuna bölmek için yapılandırın.
// "LineBetween" özelliğini "true" olarak ayarlayın, böylece sütunlar arasında bir ayırma çizgisi konur.
// "LineBetween" özelliğini "false" olarak ayarlayın, böylece sütunlar arasındaki boşluk boş kalır.
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_LineBetween(lineBetween);
columns->SetCount(3);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 3.");

doc->Save(get_ArtifactsDir() + u"PageSetup.VerticalLineBetweenColumns.docx");
```

## Ayrıca Bakınız

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
