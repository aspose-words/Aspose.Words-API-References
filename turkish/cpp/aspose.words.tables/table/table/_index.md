---
title: "Aspose::Words::Tables::Table::Table yapıcı"
linktitle: "Table"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::Table yapıcı. C++'da Table sınıfının yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


[Table](../) sınıfının yeni bir örneğini başlatır.

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Sahip belge. |
## Açıklamalar


[Table](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve [ParentNode](../../../aspose.words/node/get_parentnode/) **null**'dır.

Belgeye [Table](../) eklemek için, tabloyu eklemek istediğiniz hikayede [InsertAfter1()</see> veya <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) kullanın.

## Örnekler



Bir tablo oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tablolar satırları içerir, satırlar hücreleri içerir, hücreler paragraf içerebilir
// koşular, şekiller ve hatta diğer tablolar gibi tipik öğelerle.
// Bir tablo üzerinde "EnsureMinimum" yöntemini çağırmak, şunun sağlanmasını garantiler
// tablonun en az bir satır, bir hücre ve bir paragrafı vardır.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Metni tablonun ilk satırındaki ilk hücreye ekleyin.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## Ayrıca Bakınız

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
